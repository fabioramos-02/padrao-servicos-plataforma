# Padrão de serviços da plataforma

Guia da **SETDIG — Secretaria-Executiva de Transformação Digital** (SGD) com o que todo serviço precisa ter para
entrar na Plataforma de Governo Digital de MS. É para quem desenvolve no **X-Forms** e no **Orquestrador**.

Publicado em <https://fabioramos-02.github.io/padrao-servicos-plataforma/>. A página visual da governança está em
`docs/apresentacao/index.html`.

## Como rodar

```bash
pip install -r requirements.txt
python -m mkdocs serve -a 127.0.0.1:8001
python -m mkdocs build --strict   # antes de publicar
```

O push no `master` publica pelo GitHub Actions (`.github/workflows/gh-pages.yml`).

O padrão de formulário mora no [estudo-formularios](https://github.com/fabioramos-02/estudo-formularios). Aqui ele só é apontado.
