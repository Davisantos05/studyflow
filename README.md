# StudyFlow 1.0

Aplicativo de estudos responsivo em React + TypeScript + Vite.

## Requisitos
- Node.js 20.19+ ou 22.12+

## Executar no VS Code
```bash
npm install
npm run dev
```
Abra o endereço exibido pelo terminal (normalmente http://localhost:5173).

## Gerar versão para publicar
```bash
npm run build
```
Os arquivos prontos ficam em `dist/`.

## Funcionalidades
- Dashboard, matérias, flashcards, calendário de revisões, estatísticas e configurações.
- Revisões com algoritmo espaçado simplificado (Errei/Difícil/Bom/Fácil).
- Gerador local de cartões: uma linha por cartão no formato `Pergunta | Resposta`.
- Backup e restauração em JSON.
- Armazenamento local via localStorage, sem autenticação nem servidor.

## Limitações atuais
- Dados não sincronizam entre dispositivos. Exporte e importe backups.
- Sem leitura de PDF ou geração real por IA nesta versão.
- O algoritmo é uma implementação simplificada, não FSRS.
- Não há banco de questões externo nem notificações automáticas.
- Não inclui service worker: a versão web precisa de conexão para carregar inicialmente.

## GitHub Pages
O `vite.config.ts` utiliza `base: './'` para funcionar em subpastas. Configure um workflow de deploy do diretório `dist` ou publique seu conteúdo em GitHub Pages.

## Privacidade
Não coloque dados sensíveis em computadores compartilhados. O armazenamento local pode ser apagado pelo navegador.

### Publicação automática sem terminal (GitHub Actions)
1. Crie um repositório chamado `studyflow` no GitHub.
2. Envie **o conteúdo da pasta `studyflow`**, inclusive a pasta oculta `.github` (não envie a pasta externa como um único diretório).
3. Em **Settings → Pages → Build and deployment → Source**, escolha **GitHub Actions**.
4. Aguarde o workflow em **Actions** terminar. O endereço será `https://SEU-USUARIO.github.io/studyflow/`.
5. Se a branch principal não se chamar `main`, ajuste o nome em `.github/workflows/deploy.yml`.

Observação: `vite.config.ts` usa `base: './'`, adequado para a publicação em subdiretório do GitHub Pages.
