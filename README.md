# Lista de Presentes — Chá de Panela (Site)

Site simples para que cada convidado **reserve um presente**, evitando itens repetidos. Feito para hospedagem estática (GitHub Pages, Vercel, Netlify etc.) e usando **Firebase** (Auth anônima + Realtime Database).

## ⚙️ Configuração Firebase
1. Crie projeto no [Firebase Console](https://console.firebase.google.com/)
2. Crie app Web (ícone </>) e copie o `firebaseConfig`.
3. Cole os dados no `app.js` (substituindo os `COLOQUE_AQUI`).
4. Ative **Authentication → Anonymous**.
5. Crie **Realtime Database** e use a URL no `databaseURL`.
6. Regras temporárias:
```json
{
  "rules": {
    ".read": true,
    ".write": "auth != null"
  }
}
