# 🚀 GraphQL API za upravljanje korisnicima

Ovo je jednostavan GraphQL API razvijen pomoću Apollo Server-a i Node.js-a. API omogućava registraciju novih korisnika i dohvatanje liste svih registrovanih korisnika.

## 📌 Funkcionalnosti
- Registracija novog korisnika (`addUser` mutacija)
- Dohvatanje svih registrovanih korisnika (`users` upit)
- Koristi memoriju servera za skladištenje podataka (podaci se brišu nakon restartovanja servera)

---

## 📦 Instalacija i pokretanje

### 🔹 Preduslovi
Pre nego što započneš, uveri se da imaš instalirano sledeće:
- [Node.js](https://nodejs.org/) (verzija 14 ili novija)
- [npm](https://www.npmjs.com/) (dolazi sa Node.js-om)
- Terminal (Command Prompt, Git Bash itd.)

### 🔹 Koraci za pokretanje API-ja
1. **Kloniraj repozitorijum**  
   ```sh
   git clone https://github.com/KORISNICKO_IME/IME_REPOZITORIJUMA.git
Uđi u projekat
sh
cd IME_REPOZITORIJUMA

Instaliraj zavisnosti
sh
npm install

Pokreni server
sh
node script.js

Ako je sve u redu, trebalo bi da vidiš poruku u terminalu:

arduino
Server je pokrenut na http://localhost:4000/
🎯 Kako koristiti API
✅ 1. Otvori Apollo Server Playground
Nakon pokretanja servera, otvori pregledač i idi na:
👉 http://localhost:4000/

✅ 2. Dohvati sve korisnike
Pokreni ovaj GraphQL upit da vidiš sve registrovane korisnike:

graphql
{
  users {
    id
    name
    email
  }
}
✅ 3. Registruj novog korisnika
Pokreni ovu mutaciju da dodaš korisnika:

graphql
mutation {
  addUser(name: "Petar Petrović", email: "petar@example.com") {
    id
    name
    email
  }
}
✅ 4. Proveri da li je korisnik sačuvan
Ponovo pokreni users upit da vidiš nove podatke.

📌 Napomene
Ovaj API ne koristi bazu podataka; svi podaci se čuvaju u memoriji servera i brišu se nakon restartovanja.
Ako želiš da podaci budu trajno sačuvani, možeš integrisati bazu podataka poput MongoDB-a ili SQLite-a.
