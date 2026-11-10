# StudyFlow 1.1

## Instalação no GitHub Pages
Envie os arquivos e pastas deste ZIP para a raiz do repositório `Davisantos05/studyflow`, substituindo os arquivos existentes. Mantenha a pasta `.github/workflows` e aguarde a ação de deploy.

## Recursos
- Gerador local de cartões: detecta frases com `é`, `são`, `significa`, `consiste em`, `refere-se a`, `é responsável por`, `tem como função`, etc.; também aceita `Pergunta | Resposta`. É um extrator por regras, **não** um modelo de IA generativa.
- Prévia editável dos cartões antes de salvar.
- Imagens na frente e no verso dos cartões; imagens são reduzidas para até 900px e comprimidas como JPEG.
- Mantém o mesmo armazenamento `studyflow-v1` do navegador, preservando cartões e revisões já existentes naquele navegador e domínio.

## Atenção
Faça backup dos dados na seção Configurações antes de atualizar. Dados locais não sincronizam automaticamente entre dispositivos. Muitas imagens podem esgotar o limite de armazenamento do navegador. A compilação não pôde ser executada neste ambiente porque as dependências npm não estavam instaladas; o GitHub Actions instalará as dependências no deploy.
