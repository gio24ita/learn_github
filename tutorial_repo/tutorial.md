---

# 🚀 Creare una repository da zero + workflow quotidiano

Questa guida spiega passo per passo come creare una nuova repository Git da una cartella locale vuota, collegarla a GitHub e fare il primo push.

---

## 📁 1. Crea o apri la tua cartella di progetto

```bash
cd mia_cartella
```

🔹 Entra nella cartella dove vuoi inizializzare il progetto.
Se la cartella non esiste ancora, creala prima con:

```bash
mkdir mia_cartella
cd mia_cartella
```

---

## 🧩 2. Inizializza Git

```bash
git init
```

🔹 Trasforma la cartella in un repository Git locale.
Crea una sottocartella nascosta `.git` che contiene la storia, i branch e i metadati del progetto.

📌 Da qui in poi, puoi usare tutti i comandi `git`.

---

## 📄 3. Crea un file README e .gitignore

```bash
echo "# Nome progetto" > README.md
echo "venv/" > .gitignore
```

🔹 Il file `README.md` serve per descrivere il progetto.
🔹 Il file `.gitignore` indica a Git quali file/cartelle non tracciare (es. ambienti virtuali Python, file temporanei, ecc.).

**Esempio di `.gitignore` più completo:**

```bash
venv/
__pycache__/
*.pyc
.env
```

---

## 🧱 4. Aggiungi e committa i file

```bash
git add .
git commit -m "Initial commit"
```

🔹 `git add .` aggiunge tutti i file alla zona di staging.
🔹 `git commit -m` crea una “fotografia” dei file attuali con un messaggio.

---

## 🌿 5. Imposta il branch principale

```bash
git branch -M main
```

🔹 Rinomina il branch corrente in **main** (standard moderno al posto di *master*).

---

## ☁️ 6. Collega la repository a GitHub

Prima **crea una repository vuota su GitHub** con lo stesso nome (ad esempio `nome_repo`), **senza** inizializzarla con un README (per evitare conflitti).

Poi collega la repo locale con:

```bash
git remote add origin https://github.com/tuoutente/nome_repo.git
```

🔹 Questo comando dice a Git dove si trova la versione “remota” del progetto (su GitHub).

Puoi verificare che sia collegata correttamente con:

```bash
git remote -v
```

---

## 📤 7. Invia il progetto su GitHub

```bash
git push -u origin main
```

🔹 Invia il branch `main` al remoto (`origin`).
🔹 L’opzione `-u` imposta il collegamento tra branch locale e remoto, così in futuro basterà usare solo `git push`.

---

## 🔁 8. Da ora in poi, workflow quotidiano

Ogni volta che modifichi il progetto:

```bash
git add .
git commit -m "Descrizione delle modifiche"
git push
```

🔹 `add` prepara i file
🔹 `commit` salva la nuova versione
🔹 `push` la invia su GitHub

---

## ✅ 9. Riepilogo dei comandi

```bash
cd mia_cartella
git init
echo "# Nome progetto" > README.md
echo "venv/" > .gitignore
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/tuoutente/nome_repo.git
git push -u origin main
```

---

📘 Ora la tua repository locale è connessa a GitHub!
Puoi lavorare, fare commit e push senza dover riconfigurare nulla.

