<p align="center"><img src="https://laravel.com/assets/img/components/logo-laravel.svg"></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/d/total.svg" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/v/stable.svg" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/license.svg" alt="License"></a>
</p>


<h3>Testing the API</h3>

To test the api, here I'm providing some demo codes in PHP. You can create an index.php file and copy paste the codes there.
<br>
<p>Please do not forgot to change the value of <b>$url</b> to your host address</p>


<h5>Demo Code to retrieve data</h3>
$url = 'http://127.0.0.1:8000/api/products'; // path to your JSON file<br>
$data = file_get_contents($url); // put the contents of the file into a variable<br>
$array = json_decode($data); // decode the JSON feed<br>

/*echo "Name: ".$array->data[0]->name;*/<br>

foreach($array->data as $single_data){<br>
    echo "Name: ". $single_data->name . " | Total Price: ". $single_data->total_price ." | Stock: ". $single_data->stock ."<br>";<br>
}<br>
