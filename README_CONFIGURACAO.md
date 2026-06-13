# Lar Buceles - Central da Família

Aplicação web responsiva feita para Marcus Buceles e Ingrid Buceles administrarem o lar com Firebase, Firestore e integração com Google Agenda.

## O que vem pronto

- `index.html`: app completo em HTML, CSS e JavaScript.
- `manifest.webmanifest`, `icon.svg` e `sw.js`: estrutura PWA para abrir melhor no celular.
- `firebase.rules`: regras iniciais de segurança do Firestore.

## Recursos do app

- Login com conta Google pelo Firebase Auth.
- Banco de dados Firestore em tempo real.
- Lar familiar compartilhado por código e PIN.
- Finanças, contas, compras, estoque, tarefas, manutenção, documentos, agenda e emergências.
- Sincronização de compromissos com Google Agenda usando Google Calendar API.
- Visual fluido, responsivo, com animações e navegação mobile.
- Assinatura: Feito por Marcus Buceles e Ingrid Buceles.

## Configuração Firebase

1. Acesse o Firebase Console.
2. Crie um projeto.
3. Adicione um app Web.
4. Ative Authentication > Sign-in method > Google.
5. Ative Firestore Database.
6. Copie o objeto `firebaseConfig`.
7. Publique as regras de `firebase.rules` no Firestore Rules.

## Configuração Google Agenda

1. Acesse Google Cloud Console.
2. No mesmo projeto ou em outro projeto, ative a Google Calendar API.
3. Configure a tela de consentimento OAuth.
4. Crie uma credencial OAuth Client ID do tipo Web Application.
5. Em Authorized JavaScript origins, adicione o domínio onde você vai hospedar o app.
6. Crie uma API Key.
7. Abra o site e cole:
   - `firebaseConfig`
   - Google OAuth Client ID
   - Google API Key

## Hospedagem recomendada

Use Firebase Hosting, Vercel, Netlify, GitHub Pages ou Base44. Para Google OAuth funcionar corretamente, evite abrir pelo `file://`; publique em um domínio HTTPS.

## Observação de segurança

As chaves web do Firebase e Google podem ficar no frontend, mas precisam estar protegidas por:

- domínios autorizados no Firebase Auth;
- restrições de domínio na API Key do Google;
- regras do Firestore;
- App Check em produção, se possível.

As regras incluídas são boas para um primeiro MVP familiar. Para um app público, recomendo implementar convites com Cloud Functions e validações mais rígidas.
