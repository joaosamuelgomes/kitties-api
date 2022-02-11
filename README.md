<div align="center">
  <img src="https://ik.imagekit.io/joaosamuelgomes/logo-header-api_MUs6bandKaJ.png?ik-sdk-version=javascript-1.4.3&updatedAt=1644579064403"/>
  <p>Esse projeto implementa a parte de back-end do site Kitties e utiliza tecnologias como Wordpress e PHP.</p>
</div>

## Tecnologias Utilizadas 🛠️

Este projeto foi criado usando as seguintes tecnologias

-   [WordPress](https://wordpress.com)
-   [Local](https://localwp.com)
-   [PHP](https://www.php.net)

## Atenção 🔴

Esse projeto implementa a parte de back-end da aplicação, o projeto que implementa as chamadas feitas aqui é o projeto [kitties-react-js](https://github.com/joaosamuelgomes/kitties-react-js).

Caso você tenha o XAMPP ou qualquer outro aplicativo que execute um servidor Apache em sua máquina é importante desliga-lo para o correto funcionamento do Local.

## Como baixar esse projeto 📦

```bash
  $git clone https://github.com/joaosamuelgomes/kitties-react-js/
```

## Como instalar e utilizar 💡

Primeiramente você irá precisar do Local instalado na sua máquina você pode fazer o download dele através do site deles através dessse [link](https://localwp.com).

Após a instalação você irá abrir o programa e verá a seguinte tela:

![Local-home](https://ik.imagekit.io/joaosamuelgomes/Screenshot_1_HMU0URiKZSr.png?ik-sdk-version=javascript-1.4.3&updatedAt=1644587303243)

Você deve ir em **CREATE A NEW SITE** no nome do site você irá colocar kittiesapi após em nome de usuário e senha você criará um padrão seu, você precisará dele mais a frente pra fazer login na tela administrativa do wordpress. em Enviroment você ira escolhere **preferred**. Após essa configuração inicial você ira no canto superior direito e clicará em **START SITE** e logo após em **W ADMIN** como mostra a figura abaixo

![Local-wadmin](https://ik.imagekit.io/joaosamuelgomes/Screenshot_7_C7OCU98eSwy.png?ik-sdk-version=javascript-1.4.3&updatedAt=1644587303560)

Você fara login no wordpress com o usuário padrão que acabou de criar

![Local-wlogin](https://ik.imagekit.io/joaosamuelgomes/Screenshot_5_pi6wAqNWL2bn.png?ik-sdk-version=javascript-1.4.3&updatedAt=1644587303263)

Após efetuar o login você irá na pasta que instalou o Local e irá colocar a pasta **api** presente nesse projeto dentro do caminho abaixo podendo deletar as demais pastas **menos o arquivo index.php**

```
Local Sites\kittiesapi\app\public\wp-content\themes
```

Dessa forma

![Local-wpasta](https://ik.imagekit.io/joaosamuelgomes/Screenshot_8_BcTjd_IdUN.png?ik-sdk-version=javascript-1.4.3&updatedAt=1644587303872)

Você voltara ao site do wordpress onde fez login ativará o tema que acabou de colocar dentro da pasta themes dessa forma

![Local-wativar](https://ik.imagekit.io/joaosamuelgomes/Screenshot_9_L9Zbt1DOE5e7.png?ik-sdk-version=javascript-1.4.3&updatedAt=1644587304245)

Vocês iram instalar o plugin **JWT Authentication for WP-API** dessa forma, mas atenção **NÃO CLIQUEM EM ATIVAR AINDA**.

![Local-wplugin](https://ik.imagekit.io/joaosamuelgomes/Screenshot_10_qMpKPca1E.png?ik-sdk-version=javascript-1.4.3&updatedAt=1644587304795)

É necessário modificar o arquivo .htaccess e inserir o seguinte código

```
RewriteEngine on
RewriteCond %{HTTP:Authorization} ^(.*)
RewriteRule ^(.*) - [E=HTTP_AUTHORIZATION:%1]
```

também e necessário modificar o wp-config.php e mudar onde está 'STRING AQUI' por uma das strings geradas nesse [site](https://api.wordpress.org/secret-key/1.1/salt/).

```
define('JWT_AUTH_SECRET_KEY', 'STRING AQUI');
define('JWT_AUTH_CORS_ENABLE', true);
```

copiando a string gerada a direita dessa forma

![Local-wstring](https://ik.imagekit.io/joaosamuelgomes/Screenshot_14_zi_RhI9Mg.png?ik-sdk-version=javascript-1.4.3&updatedAt=1644589355913)

Após isso você ativa o plugin e da refresh nas rotas indo em settings, permalinks e salvando a configuração novamente, dessa forma

![Local-wrefresh](https://ik.imagekit.io/joaosamuelgomes/Screenshot_13_x2Kc39RwV9.png?ik-sdk-version=javascript-1.4.3&updatedAt=1644587305418)

## Considerações Finais 🚀

Esse projeto foi criado com base no curso de WordPress API da [Origamid](https://www.origamid.com) e tem o intuito de relembrar conceitos de banco de dados, API, servidor WordPress e aprimorar habilidades de PHP.
