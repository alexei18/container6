# Containers06

## Numele lucrării de laborator

Lucrarea de laborator este intitulată "Containers06".

## Scopul lucrării

Scopul lucrării este de a implementa un mediu de dezvoltare bazat pe containere Docker pentru un site PHP, utilizând servicii precum nginx, PHP-FPM și MySQL.

## Sarcina

- Implementarea unui mediu de dezvoltare cu containere Docker.
- Configurarea unui server nginx pentru a servi pagini PHP.
- Utilizarea PHP-FPM pentru a gestiona cererile PHP.
- Utilizarea unui container MySQL pentru stocarea datelor.

## Descrierea efectuării lucrării cu răspunsuri la întrebări

1. **Crearea structurii de directoare și fișiere:**

   - Am creat directorul `containers06`.
   - Am creat subdirectoarele `mounts/site` și `nginx`.
   - Am creat fișierele `.gitignore`, `docker-compose.yml`, `mysql.env`, și `README.md`.

2. **Configurarea fișierelor de configurare:**

   - Am configurat `nginx/default.conf` pentru a gestiona cererile HTTP și PHP.
   - Am configurat `docker-compose.yml` pentru a defini serviciile și dependențele lor.

3. **Pornirea containerele:**

   - Am pornit containerele utilizând comanda `docker-compose up -d`.

4. **Testarea funcționării site-ului:**
   - Am accesat adresa `http://localhost` în browser și am verificat dacă site-ul PHP este afișat corect.

## Concluzii

Proiectul containers06 demonstrează implementarea unui mediu de dezvoltare folosind containere Docker pentru a executa un site PHP. Prin configurarea serviciilor precum nginx, PHP-FPM și MySQL, putem crea un mediu de dezvoltare izolat și ușor de gestionat pentru proiectele noastre.

## Răspunsuri la întrebări:

1. **În ce ordine sunt pornite containerele?**

   - Containerele sunt pornite în ordinea în care sunt definite în fișierul `docker-compose.yml`. În acest caz, se pornesc mai întâi containerele `frontend`, `backend`, și `database`.

2. **Unde sunt stocate datele bazei de date?**

   - Datele bazei de date sunt stocate într-un volum Docker numit `db_data`, care este definit în fișierul `docker-compose.yml`.

3. **Cum se numesc containerele proiectului?**

   - Containerele proiectului sunt numite `frontend`, `backend`, și `database`.

4. **Trebuie să adăugați încă un fișier `app.env` cu variabila de mediu `APP_VERSION` pentru serviciile backend și frontend. Cum se face acest lucru?**
   - Pentru a adăuga un fișier `app.env` cu variabila de mediu `APP_VERSION` pentru serviciile backend și frontend, trebuie să creați mai întâi fișierul `app.env` și să adăugați variabila de mediu în el. Apoi, în fișierul `docker-compose.yml`, adăugați secțiunea `env_file` pentru fiecare serviciu, indicând calea către fișierul `app.env`. Astfel, variabila de mediu va fi încărcată în mediu pentru serviciile respective.
