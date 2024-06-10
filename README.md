#Lab 11

docker compose byl zainstalowany domyslne w Docker Desktop


dalej utworzłam folder projektu i umiescilam tam wszystkie potrzebne pliki, ktore znajduja sie na repo na github

uruchamiłam za pomoca polecenia(uruchomienie w trybie -detach):

docker-compose up -d

sprawdzic dzialanie uslug mozna za pomoca polecenia:

docker-compose ps

dzialanie aplikacji tak samo  potwierdzamy   saprawdzajac strony localhost'a na portach 4001 oraz 6001:
wyswietlenie strony na porcie 4001 oznacza, że Nginx i PHP-FPM dzialaja poprawnie

wyswietlenie strony na porcie 6001 oznacza, że phpMyAdmin dziala poprawnie.

Dodatkowo się polączylam z serwerem MySQL z poziomu kontenera za pomocą narzędzia mysql, aby sprawdzic dzialanie oraz zalozyc przykladowa baze:
polecenie:

docker exec -it zad_l11_l12-mysql-1 mysql -u root -p


#Lab12
Zadanie z lab 11 bylo zmodyfikowano:

plik docker-compose byl podzielony na pliki bazowy oraz plik override(nowa struktura umieszczona jest na repo)

oraz dodane pliki mysql_root_password.txt i mysql_password.txt, aby wykorzystac ich jako sekrety. Tych plikow
nie bedzie na repo na github, ich trzeba bedzie utworzyc w folderze roboczym, gdzie znajduja sie pliki compose
zawartosc tych plikow, przypominam, bedzie znajdowala sie w pliku tekstowym z zadaniem na moodle

zatrzymanie uslug realizuje sie za pomoca polecenia:

docker-compose down
