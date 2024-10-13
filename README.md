# Laravel_Docker
laravel subdomain solution ( docker desktop ) 



<br/><br/><br/><br/>

### 11. Ensure Docker configuration files have correct ownership

```
sudo chown -R medaminebentaieb:staff /Users/medaminebentaieb/.docker
```

### Navigate to the main project directory
```
cd /Users/medaminebentaieb/Docker_files/Laravel_Docker
````

### Build and run Docker containers
```
docker-compose up -d --build
```



<br/>

---

<br/><br/><br/><br/>


### 7. Rebuild and Run Docker Containers Without Cache

**1. Navigate to the main project directory**
```
cd /Users/medaminebentaieb/Docker_files/Laravel_Docker
```

**2. Rebuild Docker images without using the cache**
```
docker-compose build --no-cache
```

**3. Start the containers in detached mode**
```
docker-compose up -d
```

<br/>

---

<br/><br/><br/><br/>



<details>
<summary>issue 1 - composer (laravel) - fruitcacke </summary>
<br>

```

medaminebentaieb@MacBook-Pro-Med Laravel_Docker % pwd 
/Users/medaminebentaieb/Docker_files/Laravel_Docker
medaminebentaieb@MacBook-Pro-Med Laravel_Docker % docker-compose up -d --build
[+] Running 31/31
 ✔ phpmyadmin Pulled                                                                                                                                              26.5s 
   ✔ faef57eae888 Pull complete                                                                                                                                    7.9s 
   ✔ 989a1d6c052e Pull complete                                                                                                                                    7.9s 
   ✔ 0705c9c2f22d Pull complete                                                                                                                                   21.4s 
   ✔ 621478e043ce Pull complete                                                                                                                                   21.4s 
   ✔ 98246dcca987 Pull complete                                                                                                                                   21.7s 
   ✔ bfed8c155cb6 Pull complete                                                                                                                                   21.7s 
   ✔ 7a7c2e908867 Pull complete                                                                                                                                   21.7s 
   ✔ d176994b625c Pull complete                                                                                                                                   21.7s 
   ✔ 2d8ace6a2716 Pull complete                                                                                                                                   21.8s 
   ✔ c70df516383c Pull complete                                                                                                                                   22.0s 
   ✔ 15e1b44fe4c7 Pull complete                                                                                                                                   22.0s 
   ✔ 65e50d44e95a Pull complete                                                                                                                                   22.0s 
   ✔ 77f68910bc0a Pull complete                                                                                                                                   22.0s 
   ✔ 605dd3a6e332 Pull complete                                                                                                                                   22.1s 
   ✔ 99ce27188f07 Pull complete                                                                                                                                   22.1s 
   ✔ 74d64e32c5d5 Pull complete                                                                                                                                   22.9s 
   ✔ ef5fc9928b9f Pull complete                                                                                                                                   22.9s 
   ✔ 163f3256e112 Pull complete                                                                                                                                   22.9s 
 ✔ db Pulled                                                                                                                                                      44.0s 
   ✔ 8b4274ea61c5 Pull complete                                                                                                                                   27.4s 
   ✔ 65b13290a890 Pull complete                                                                                                                                   27.4s 
   ✔ 4a0edbf0dd13 Pull complete                                                                                                                                   27.4s 
   ✔ f8d978a6739e Pull complete                                                                                                                                   27.5s 
   ✔ 64da6e9087ad Pull complete                                                                                                                                   27.6s 
   ✔ f6d5909e94cd Pull complete                                                                                                                                   27.6s 
   ✔ 949fd89ec12a Pull complete                                                                                                                                   33.2s 
   ✔ 5355ea40a182 Pull complete                                                                                                                                   33.2s 
   ✔ 2a489f3632fa Pull complete                                                                                                                                   40.0s 
   ✔ efd64d077766 Pull complete                                                                                                                                   40.0s 
   ✔ e6689b530d4e Pull complete                                                                                                                                   40.0s 
[+] Building 271.7s (13/16)                                                                                                                        docker:desktop-linux
[+] Building 271.8s (13/16)                                                                                                                        docker:desktop-linux
[+] Building 272.0s (13/16)                                                                                                                        docker:desktop-linux
[+] Building 309.2s (14/16)                                                                                                                        docker:desktop-linux
 => [laravel internal] load build definition from Dockerfile                                                                                                       0.0s
 => => transferring dockerfile: 988B                                                                                                                               0.0s
 => [laravel internal] load metadata for docker.io/library/composer:latest                                                                                         1.0s
 => [laravel internal] load metadata for docker.io/library/php:8.2-fpm                                                                                             1.1s
 => [laravel auth] library/composer:pull token for registry-1.docker.io                                                                                            0.0s
 => [laravel auth] library/php:pull token for registry-1.docker.io                                                                                                 0.0s
 => [laravel internal] load .dockerignore                                                                                                                          0.0s
 => => transferring context: 2B                                                                                                                                    0.0s
 => [laravel stage-0 1/8] FROM docker.io/library/php:8.2-fpm@sha256:44323764bd7ff0a64acf1e8d162315b5188e7917959eec1b8d5d7c726fad1558                               0.0s
 => [laravel internal] load build context                                                                                                                          0.0s
 => => transferring context: 17.50kB                                                                                                                               0.0s
 => [laravel] FROM docker.io/library/composer:latest@sha256:a9b32ddde7df8f87b714fe6e833d601014abb02e2c02e68d7d0405e3ce423cc3                                       0.0s
 => CACHED [laravel stage-0 2/8] RUN apt-get update && apt-get install -y     build-essential     libpng-dev     libonig-dev     libxml2-dev     zip     unzip     0.0s
 => CACHED [laravel stage-0 3/8] COPY --from=composer:latest /usr/bin/composer /usr/bin/composer                                                                   0.0s
 => CACHED [laravel stage-0 4/8] WORKDIR /var/www                                                                                                                  0.0s
 => CACHED [laravel stage-0 5/8] COPY src/ /var/www                                                                                                                0.0s
 => ERROR [laravel stage-0 6/8] RUN composer install --optimize-autoloader --no-dev                                                                              308.0s
------                                                                                                                                                                  
 > [laravel stage-0 6/8] RUN composer install --optimize-autoloader --no-dev:                                                                                           
0.238 Installing dependencies from lock file                                                                                                                            
0.240 Verifying lock file contents can be installed on current platform.                                                                                                
0.249 Package operations: 94 installs, 0 updates, 0 removals                                                                                                            
0.250   - Downloading symfony/polyfill-ctype (v1.30.0)                                                                                                                  
0.250   - Downloading symfony/polyfill-php83 (v1.30.0)
0.251   - Downloading symfony/polyfill-mbstring (v1.30.0)
0.251   - Downloading symfony/deprecation-contracts (v3.5.0)
0.251   - Downloading symfony/http-foundation (v6.4.10)
0.251   - Downloading psr/event-dispatcher (1.0.0)
0.251   - Downloading symfony/event-dispatcher-contracts (v3.5.0)
0.251   - Downloading symfony/event-dispatcher (v7.1.1)
0.252   - Downloading symfony/var-dumper (v6.4.10)
0.252   - Downloading psr/log (3.0.0)
0.252   - Downloading symfony/error-handler (v6.4.10)
0.252   - Downloading symfony/http-kernel (v6.4.10)
0.252   - Downloading voku/portable-ascii (2.0.1)
0.252   - Downloading symfony/polyfill-php80 (v1.30.0)
0.252   - Downloading phpoption/phpoption (1.9.3)
0.253   - Downloading graham-campbell/result-type (v1.1.3)
0.253   - Downloading vlucas/phpdotenv (v5.6.1)
0.253   - Downloading symfony/css-selector (v7.1.1)
0.253   - Downloading tijsverkoyen/css-to-inline-styles (v2.2.7)
0.253   - Downloading symfony/polyfill-uuid (v1.30.0)
0.253   - Downloading symfony/uid (v6.4.8)
0.253   - Downloading symfony/routing (v6.4.10)
0.253   - Downloading symfony/process (v6.4.8)
0.253   - Downloading symfony/polyfill-php72 (v1.30.0)
0.253   - Downloading symfony/polyfill-intl-normalizer (v1.30.0)
0.253   - Downloading symfony/polyfill-intl-idn (v1.30.0)
0.253   - Downloading symfony/mime (v6.4.9)
0.253   - Downloading psr/container (2.0.2)
0.253   - Downloading symfony/service-contracts (v3.5.0)
0.254   - Downloading doctrine/lexer (3.0.1)
0.254   - Downloading egulias/email-validator (4.0.2)
0.254   - Downloading symfony/mailer (v6.4.9)
0.254   - Downloading symfony/finder (v6.4.10)
0.254   - Downloading symfony/polyfill-intl-grapheme (v1.30.0)
0.254   - Downloading symfony/string (v7.1.3)
0.254   - Downloading symfony/console (v6.4.10)
0.254   - Downloading ramsey/collection (2.0.0)
0.255   - Downloading brick/math (0.12.1)
0.255   - Downloading ramsey/uuid (4.7.6)
0.255   - Downloading psr/simple-cache (3.0.0)
0.255   - Downloading nunomaduro/termwind (v1.15.1)
0.255   - Downloading symfony/translation-contracts (v3.5.0)
0.255   - Downloading symfony/translation (v6.4.10)
0.255   - Downloading psr/clock (1.0.0)
0.255   - Downloading carbonphp/carbon-doctrine-types (2.1.0)
0.255   - Downloading nesbot/carbon (2.72.5)
0.255   - Downloading monolog/monolog (3.7.0)
0.256   - Downloading league/mime-type-detection (1.15.0)
0.256   - Downloading league/flysystem (3.28.0)
0.256   - Downloading league/flysystem-local (3.28.0)
0.256   - Downloading nette/utils (v4.0.5)
0.256   - Downloading nette/schema (v1.3.0)
0.256   - Downloading dflydev/dot-access-data (v3.0.3)
0.256   - Downloading league/config (v1.2.0)
0.256   - Downloading league/commonmark (2.5.2)
0.256   - Downloading laravel/serializable-closure (v1.3.4)
0.257   - Downloading laravel/framework (v10.48.20)
0.257   - Downloading laravel/prompts (v0.1.24)
0.257   - Downloading guzzlehttp/uri-template (v1.0.3)
0.257   - Downloading fruitcake/php-cors (v1.3.0)
0.257   - Downloading webmozart/assert (1.11.0)
0.257   - Downloading dragonmantank/cron-expression (v3.3.3)
0.257   - Downloading doctrine/inflector (2.0.10)
0.257   - Downloading asm89/stack-cors (v2.2.0)
0.257   - Downloading barryvdh/laravel-cors (dev-develop 8cf8697)
0.257   - Downloading sabberworm/php-css-parser (v8.6.0)
0.258   - Downloading phenx/php-svg-lib (0.5.4)
0.258   - Downloading phenx/php-font-lib (0.5.6)
0.258   - Downloading masterminds/html5 (2.9.0)
0.258   - Downloading dompdf/dompdf (v2.0.8)
0.258   - Downloading barryvdh/laravel-dompdf (v2.2.0)
0.258   - Downloading fruitcake/laravel-cors (dev-develop 8cf8697)
0.258   - Downloading psr/http-message (2.0)
0.258   - Downloading psr/http-client (1.0.3)
0.258   - Downloading ralouphie/getallheaders (3.0.3)
0.258   - Downloading psr/http-factory (1.1.0)
0.258   - Downloading guzzlehttp/psr7 (2.7.0)
0.258   - Downloading guzzlehttp/promises (2.0.3)
0.258   - Downloading guzzlehttp/guzzle (7.9.2)
0.259   - Downloading laravel/sanctum (v3.3.3)
0.259   - Downloading setasign/fpdi (v2.6.1)
0.259   - Downloading paragonie/random_compat (v9.99.100)
0.259   - Downloading myclabs/deep-copy (1.12.0)
0.259   - Downloading mpdf/psr-log-aware-trait (v3.0.0)
0.259   - Downloading mpdf/psr-http-message-shim (v2.0.1)
0.260   - Downloading mpdf/mpdf (v8.2.4)
0.260   - Downloading namshi/jose (7.2.3)
0.260   - Downloading lcobucci/jwt (5.3.0)
0.260   - Downloading php-open-source-saver/jwt-auth (2.7.1)
0.260   - Downloading spatie/laravel-package-tools (1.16.4)
0.260   - Downloading rappasoft/laravel-authentication-log (v3.0.0)
0.260   - Downloading setasign/fpdf (1.8.6)
0.260   - Downloading torann/geoip (3.0.8)
0.314   0/93 [>---------------------------]   0%
1.218  13/93 [===>------------------------]  13%
1.547  20/93 [======>---------------------]  21%
1.757  28/93 [========>-------------------]  30%
2.841  37/93 [===========>----------------]  39%
2.967  38/93 [===========>----------------]  40%
4.023  40/93 [============>---------------]  43%
5.076  44/93 [=============>--------------]  47%
6.156  48/93 [==============>-------------]  51%
7.162  54/93 [================>-----------]  58%
8.325  56/93 [================>-----------]  60%
9.425  57/93 [=================>----------]  61%
10.50  61/93 [==================>---------]  65%
11.57  62/93 [==================>---------]  66%
12.64  63/93 [==================>---------]  67%
13.74  64/93 [===================>--------]  68%
14.83  66/93 [===================>--------]  70%
15.90  73/93 [=====================>------]  78%
16.98  74/93 [======================>-----]  79%
19.25  75/93 [======================>-----]  80%
20.26  80/93 [========================>---]  86%
21.28  81/93 [========================>---]  87%
22.34  82/93 [========================>---]  88%
23.38  83/93 [========================>---]  89%
23.50  85/93 [=========================>--]  91%
24.54  86/93 [=========================>--]  92%
25.65  87/93 [==========================>-]  93%
26.68  88/93 [==========================>-]  94%
27.80  89/93 [==========================>-]  95%
30.33  90/93 [===========================>]  96%
35.88  91/93 [===========================>]  97%
56.71  92/93 [===========================>]  98%
306.2  93/93 [============================] 100%
306.2   - Installing symfony/polyfill-ctype (v1.30.0): Extracting archive
306.2   - Installing symfony/polyfill-php83 (v1.30.0): Extracting archive
306.2   - Installing symfony/polyfill-mbstring (v1.30.0): Extracting archive
306.2   - Installing symfony/deprecation-contracts (v3.5.0): Extracting archive
306.2   - Installing symfony/http-foundation (v6.4.10): Extracting archive
306.2   - Installing psr/event-dispatcher (1.0.0): Extracting archive
306.2   - Installing symfony/event-dispatcher-contracts (v3.5.0): Extracting archive
306.2   - Installing symfony/event-dispatcher (v7.1.1): Extracting archive
306.2   - Installing symfony/var-dumper (v6.4.10): Extracting archive
306.2   - Installing psr/log (3.0.0): Extracting archive
306.2   - Installing symfony/error-handler (v6.4.10): Extracting archive
306.2   - Installing symfony/http-kernel (v6.4.10): Extracting archive
306.2   - Installing voku/portable-ascii (2.0.1): Extracting archive
306.3   - Installing symfony/polyfill-php80 (v1.30.0): Extracting archive
306.3   - Installing phpoption/phpoption (1.9.3): Extracting archive
306.3   - Installing graham-campbell/result-type (v1.1.3): Extracting archive
306.3   - Installing vlucas/phpdotenv (v5.6.1): Extracting archive
306.3   - Installing symfony/css-selector (v7.1.1): Extracting archive
306.3   - Installing tijsverkoyen/css-to-inline-styles (v2.2.7): Extracting archive
306.3   - Installing symfony/polyfill-uuid (v1.30.0): Extracting archive
306.3   - Installing symfony/uid (v6.4.8): Extracting archive
306.3   - Installing symfony/routing (v6.4.10): Extracting archive
306.3   - Installing symfony/process (v6.4.8): Extracting archive
306.3   - Installing symfony/polyfill-php72 (v1.30.0): Extracting archive
306.3   - Installing symfony/polyfill-intl-normalizer (v1.30.0): Extracting archive
306.3   - Installing symfony/polyfill-intl-idn (v1.30.0): Extracting archive
306.3   - Installing symfony/mime (v6.4.9): Extracting archive
306.3   - Installing psr/container (2.0.2): Extracting archive
306.3   - Installing symfony/service-contracts (v3.5.0): Extracting archive
306.3   - Installing doctrine/lexer (3.0.1): Extracting archive
306.3   - Installing egulias/email-validator (4.0.2): Extracting archive
306.3   - Installing symfony/mailer (v6.4.9): Extracting archive
306.3   - Installing symfony/finder (v6.4.10): Extracting archive
306.3   - Installing symfony/polyfill-intl-grapheme (v1.30.0): Extracting archive
306.3   - Installing symfony/string (v7.1.3): Extracting archive
306.3   - Installing symfony/console (v6.4.10): Extracting archive
306.3   - Installing ramsey/collection (2.0.0): Extracting archive
306.3   - Installing brick/math (0.12.1): Extracting archive
306.3   - Installing ramsey/uuid (4.7.6): Extracting archive
306.3   - Installing psr/simple-cache (3.0.0): Extracting archive
306.3   - Installing nunomaduro/termwind (v1.15.1): Extracting archive
306.3   - Installing symfony/translation-contracts (v3.5.0): Extracting archive
306.3   - Installing symfony/translation (v6.4.10): Extracting archive
306.3   - Installing psr/clock (1.0.0): Extracting archive
306.3   - Installing carbonphp/carbon-doctrine-types (2.1.0): Extracting archive
306.3   - Installing nesbot/carbon (2.72.5): Extracting archive
306.3   - Installing monolog/monolog (3.7.0): Extracting archive
306.3   - Installing league/mime-type-detection (1.15.0): Extracting archive
306.3   - Installing league/flysystem (3.28.0): Extracting archive
306.3   - Installing league/flysystem-local (3.28.0): Extracting archive
306.3   - Installing nette/utils (v4.0.5): Extracting archive
306.3   - Installing nette/schema (v1.3.0): Extracting archive
306.3   - Installing dflydev/dot-access-data (v3.0.3): Extracting archive
306.3   - Installing league/config (v1.2.0): Extracting archive
306.3   - Installing league/commonmark (2.5.2): Extracting archive
306.3   - Installing laravel/serializable-closure (v1.3.4): Extracting archive
306.3   - Installing laravel/framework (v10.48.20): Extracting archive
306.3   - Installing laravel/prompts (v0.1.24): Extracting archive
306.3   - Installing guzzlehttp/uri-template (v1.0.3): Extracting archive
306.3   - Installing fruitcake/php-cors (v1.3.0): Extracting archive
306.3   - Installing webmozart/assert (1.11.0): Extracting archive
306.3   - Installing dragonmantank/cron-expression (v3.3.3): Extracting archive
306.3   - Installing doctrine/inflector (2.0.10): Extracting archive
306.3   - Installing asm89/stack-cors (v2.2.0): Extracting archive
306.3   - Installing barryvdh/laravel-cors (dev-develop 8cf8697): Extracting archive
306.3   - Installing sabberworm/php-css-parser (v8.6.0): Extracting archive
306.3   - Installing phenx/php-svg-lib (0.5.4): Extracting archive
306.3   - Installing phenx/php-font-lib (0.5.6): Extracting archive
306.3   - Installing masterminds/html5 (2.9.0): Extracting archive
306.3   - Installing dompdf/dompdf (v2.0.8): Extracting archive
306.3   - Installing barryvdh/laravel-dompdf (v2.2.0): Extracting archive
306.3   - Installing fruitcake/laravel-cors (dev-develop 8cf8697): Extracting archive
306.3   - Installing psr/http-message (2.0): Extracting archive
306.3   - Installing psr/http-client (1.0.3): Extracting archive
306.3   - Installing ralouphie/getallheaders (3.0.3): Extracting archive
306.3   - Installing psr/http-factory (1.1.0): Extracting archive
306.3   - Installing guzzlehttp/psr7 (2.7.0): Extracting archive
306.3   - Installing guzzlehttp/promises (2.0.3): Extracting archive
306.3   - Installing guzzlehttp/guzzle (7.9.2): Extracting archive
306.3   - Installing laravel/sanctum (v3.3.3): Extracting archive
306.3   - Installing setasign/fpdi (v2.6.1): Extracting archive
306.3   - Installing paragonie/random_compat (v9.99.100): Extracting archive
306.3   - Installing myclabs/deep-copy (1.12.0): Extracting archive
306.3   - Installing mpdf/psr-log-aware-trait (v3.0.0): Extracting archive
306.3   - Installing mpdf/psr-http-message-shim (v2.0.1): Extracting archive
306.3   - Installing mpdf/mpdf (v8.2.4): Extracting archive
306.3   - Installing symfony/polyfill-php56 (v1.20.0)
306.3   - Installing namshi/jose (7.2.3): Extracting archive
306.3   - Installing lcobucci/jwt (5.3.0): Extracting archive
306.3   - Installing php-open-source-saver/jwt-auth (2.7.1): Extracting archive
306.3   - Installing spatie/laravel-package-tools (1.16.4): Extracting archive
306.3   - Installing rappasoft/laravel-authentication-log (v3.0.0): Extracting archive
306.3   - Installing setasign/fpdf (1.8.6): Extracting archive
306.3   - Installing torann/geoip (3.0.8): Extracting archive
306.3   0/93 [>---------------------------]   0%
306.4  60/93 [==================>---------]  64%
306.5  92/93 [===========================>]  98%
307.0  93/93 [============================] 100%
307.3 Package barryvdh/laravel-cors is abandoned, you should avoid using it. No replacement was suggested.
307.3 Package fruitcake/laravel-cors is abandoned, you should avoid using it. No replacement was suggested.
307.3 Generating optimized autoload files
307.8 Warning: Ambiguous class resolution, "Fruitcake\Cors\CorsServiceProvider" was found in both "/var/www/vendor/barryvdh/laravel-cors/src/CorsServiceProvider.php" and "/var/www/vendor/fruitcake/laravel-cors/src/CorsServiceProvider.php", the first will be used.
307.8 Warning: Ambiguous class resolution, "Fruitcake\Cors\HandleCors" was found in both "/var/www/vendor/barryvdh/laravel-cors/src/HandleCors.php" and "/var/www/vendor/fruitcake/laravel-cors/src/HandleCors.php", the first will be used.
307.8 > Illuminate\Foundation\ComposerScripts::postAutoloadDump
307.8 > @php artisan package:discover --ansi
307.9 
307.9 In CacheManager.php line 88:
307.9                                                  
307.9   Cache store [${CACHE_DRIVER}] is not defined.  
307.9                                                  
307.9 
307.9 Script @php artisan package:discover --ansi handling the post-autoload-dump event returned with error code 1
------
failed to solve: process "/bin/sh -c composer install --optimize-autoloader --no-dev" did not complete successfully: exit code: 1
medaminebentaieb@MacBook-Pro-Med Laravel_Docker % 
medaminebentaieb@MacBook-Pro-Med Laravel_Docker % 
medaminebentaieb@MacBook-Pro-Med Laravel_Docker % 
medaminebentaieb@MacBook-Pro-Med Laravel_Docker % 

```

</details>
 

