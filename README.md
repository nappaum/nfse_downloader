# NFS-e Nacional Downloader

Aplicativo Python com interface gráfica para apoiar o download manual assistido de arquivos XML e DANFSe (PDF) no portal nacional da NFS-e.

O fluxo é simples:

1. Abrir o portal da NFS-e no navegador automatizado.
2. Permitir que o usuário faça login manualmente.
3. Aplicar filtros por período.
4. Percorrer as páginas de resultados.
5. Baixar XMLs e/ou DANFSe para uma pasta escolhida.

## Avisos

- Este repositório foi preparado para publicação pública e não contém credenciais, dados de clientes, caminhos locais nem artefatos de build.
- O login no portal é feito manualmente pelo usuário.
- O comportamento do robô depende da estrutura atual do portal da NFS-e; mudanças no site podem exigir ajustes nos seletores.

## Requisitos

- Python 3.10 ou superior
- Windows com interface gráfica

## Instalação

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
python -m playwright install chromium
```

## Execução

```bash
python nfse_downloader_gui.py
```

## Empacotamento opcional com PyInstaller

```bash
pyinstaller nfse_downloader_gui.spec
```

## Estrutura

- `nfse_downloader_gui.py`: aplicação principal com GUI em Tkinter e automação via Playwright.
- `nfse_downloader_gui.spec`: arquivo opcional para gerar executável com PyInstaller.

## Boas práticas

- Não versione arquivos baixados, capturas de tela, logs ou navegadores instalados localmente.
- Se precisar configurar destinos ou parâmetros específicos do seu ambiente, prefira variáveis locais e arquivos ignorados pelo Git.
