# Soluzione Esercizio 02 - Branch e Merge con due branch

## 1: Assicurati di essere sul branch main
```bash
git checkout main
```

## 2: Creare e spostarsi sul nuovo branch
```bash
git checkout -b nuovo_branch
```

## 3: Modificare README.md nel branch nuovo_branch

## 4: Commit delle modifiche sul nuovo_branch
```bash
git add README.md
git commit -m "Aggiunge sezione nuovo_branch al README"
```

## 5: Creare e spostarsi sul nuovo branch
```bash
git checkout main
```

## 6: Modificare README.md sul branch main

## 7: Commit delle modifiche sul main
```bash
git add README.md
git commit -m "Aggiunge sezione main al README"
```

## 8: Fare il merge del branch nuovo_branch in main
```bash
git merge nuovo_branch
```

## 9: Push del branch main aggiornato su GitHub
```bash
git push origin main
```

## 10 (opzionale): Pulire i branch
Cancella il branch locale se non serve più:
```bash
git branch -d nuovo_branch
```

Cancella il branch remoto se non serve più:
```bash
git branch -d nuovo_branch
```


