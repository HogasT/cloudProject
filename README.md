Proiect Cloud Computing  -  Hogas Toma  -  Grupa 1133

1.Introducere
Această documentație prezintă platforma de management a unei flote de mașini, dezvoltată folosind tehnologiile Next.js pentru partea de frontend și MongoDB pentru partea de bază de date. Proiectul este găzduit pe platforma Vercel, asigurând astfel scalabilitate și performanță.
2.Descriere problemă
Platforma a fost dezvoltată pentru a gestiona eficient o flotă de mașini. Problema abordată constă în centralizarea și automatizarea proceselor de management, precum înregistrarea, actualizarea, ștergerea și monitorizarea mașinilor.
3.Descriere API
Platforma oferă un API RESTful pentru a permite operațiile CRUD (Create, Read, Update, Delete) asupra mașinilor. API-ul acceptă și returnează date în format JSON. Mai jos sunt detaliate aspectele principale ale API-ului:
  Exemple de Request/Response:
    Adaugare masina: Request
      POST /records/create:
      Body:
      {
      "maker": "Audi",
      "model": "A6",
      }
    Response
      Body:
      {
      "status": 200
      }
    Afisare toate masinile: Request
      GET /records
    Response:
      {
        "success": true,
        "cars": [
            {
              "_id": 6635027b618bfc80039bc3b9,
              "maker": "Volkswagen",
              "model": "Jetta"
            }
            ...
          ]
      }
Metode HTTP: Platforma utilizează următoarele metode HTTP:
GET pentru obținerea datelor
POST pentru adăugarea de date noi
PUT pentru actualizarea datelor existente
DELETE pentru ștergerea datelor
API-ul nu necesită autentificare sau autorizare pentru a accesa funcționalitățile CRUD.
4.Flux de date
Platforma utilizează un flux de date simplu pentru a permite interacțiunea cu baza de date MongoDB. Datele sunt trimise către și primite de la serverul Next.js, care apoi interacționează cu baza de date pentru a efectua operațiile CRUD solicitate de utilizator.
5.Capturi ecran aplicatie
![image](https://github.com/HogasT/cloudProject/assets/101126412/028d5bf2-33f1-4767-964c-3844ae442e0e) Ecran Principal
![image](https://github.com/HogasT/cloudProject/assets/101126412/1087d384-4cd7-4a30-8d9d-ccc8ef6b093a) Ecran Edit
![image](https://github.com/HogasT/cloudProject/assets/101126412/bfec1065-79a7-44d9-a0fa-5b5970d895ec) Ecran Add
6.Referințe
Next.js: https://nextjs.org/docs/getting-started
MongoDB: https://docs.mongodb.com/
Vercel: https://vercel.com/docs



