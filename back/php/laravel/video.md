Lien : https://www.youtube.com/watch?v=MT-GJQIY3EU

Routes dans API
exemple : 
```PHP
Route::get('/products', function(){
	return 'products';
});
```

Dans postman après avoir lancer le serveur aller dans la catégorie get, taper l'url (/api/products si on reprend l'exemple) et voir que Postman voit bien ce qu'il y a 

Pour avoir tous les utilisateurs dans Postman, on fait dans le get : 

```php
Route::get('/products', function() {
	return Product::all();
})
```

(remplacer product par user).

Dans user controller : 

Supprimer : 

```php
public function destroy($id)
{
	return Product::destroy($id);
}
```

Rechercher : 

```php
public function search($name)
{
	return Product::where('name', 'like', '%'.$name.'%')->get();
}
```

Dans API.php

```php

```

Créer un "register" : 

```bash
php artisan make:controller AuthController
```

```php
use App\Models\User;
use Illuminate\Httpp\Request;
use Illuminate\Http\Response;
use Illuminate\Http\Facades\Hash; (trouver où il est)
```

(Pour demander à avoir tout)

```php
class AuthController extends Controller
{
	public function register(Request $request) {
		$fields = $request->validate([
			'FirstName' => 'required|string',
			'LasName' => 'required|string',
			'Email' => 'required|string|unique:users,email',
			'Password' => 'required|string|confirmed'
		]);
		
		$user = User::create([
			'FirstName' => $fields['FirstName'],
			'LastName' => $fields['LastName'],
			'Password' => bcrypt($fields['Password']) (vérifier si on utilise                toujours ça ou pas)
		]),
		
		$token = $user->createToken('nom_du_token')->plainTextToken;
		
		$response = [
			'user' => $user,
			'token' => $token
		];
		
		return response($response, 201);
	}
}
```

![[Pasted image 20260224122938.png]]

```php
public function logout(Request $request) {
	auth()->user()->tokens()->delete();
	return[
		'message' => 'logged out'
	];
}
```

Login :

```php
public function login(Request $request){
	$fields = $request->validate([
		'email' => 'required|string|unique:users,email',
		'password' => 'required|string|confirmed'
	]);
}
```