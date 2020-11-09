# symfonyruhabolt
Symfony keretrendszerben egy ruhabolt induló projekt

##Beüzemelési lépések:
###1. Telepítés:
- symfony new symfonyruhabolt --full
- cd symfonyruhabolt/
- symfony server:start

###2. Beállítás:
- composer require symfony/orm-pack
- composer require --dev symfony/maker-bundle

.ENV fájl: DATABASE_URL="mysql://db_user:db_password@127.0.0.1:3306/db_name?serverVersion=5.7"
DATABASE_URL="mysql://root:@127.0.0.1:3306/ruhabolt?serverVersion=5.7"

###3. Első oldalak:
- php bin/console make:controller
> DefaultController

Megadjuk a twig template fájlt a render-nek és átadjuk a paramétereket amivel majd a template fájlban dolgozunk.
Kapcsos zárójelek között megadjuk a template twig fájlnak a body tag között a kiiratandó message változóban lévő értéket.

###4. Adatbázis:

Adatbázis migrációhoz fájl, kérni fogja a fájl nevét majd megint enter (php fájlban adunk hozzá plusz mezőket):
- php bin/console make:entity