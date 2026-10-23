# Catálogo de Filmes — Lumière

Versão adaptada de uma atividade Django de consulta à API OMDb. Os nomes do projeto,
do aplicativo, dos arquivos e de algumas estruturas foram reorganizados em português.
O resultado continua sendo a página **Lumière**, que apresenta filmes de Harry Potter
com pôster e título, além do texto dos cartões.

## Como executar

1. Abra o terminal na pasta `catalogo_filmes` (a que contém `manage.py`).
2. Instale as dependências:

   ```bash
   python -m pip install -r ../requirements.txt
   ```

3. Execute as migrações iniciais do Django:

   ```bash
   python manage.py migrate
   ```

4. Inicie o servidor:

   ```bash
   python manage.py runserver
   ```

5. Acesse http://127.0.0.1:8000/ no navegador.

**Observação:** os filmes são consultados online. É necessária conexão com a internet e
uma chave válida para a API OMDb. A chave demonstrativa presente no código de origem foi
mantida como valor padrão, mas pode ser substituída com a variável de ambiente
`OMDB_API_KEY`. Para ambientes publicados, configure também `DJANGO_SECRET_KEY` e
`DJANGO_DEBUG` de maneira adequada.

## Como o código está organizado

- `catalogo_filmes/catalogo_filmes/`: configurações, URLs e inicialização Django.
- `catalogo_filmes/filmes/views.py`: busca os filmes na OMDb e monta o contexto da página.
- `catalogo_filmes/filmes/templates/filmes/catalogo.html`: página com os cartões.
- `catalogo_filmes/filmes/static/filmes/catalogo.css`: estilos da página.

## Referência

Adaptação educacional do repositório
[danieloribeiro/AtividadeAula2](https://github.com/danieloribeiro/AtividadeAula2).
A licença MIT e os avisos de copyright do arquivo `LICENSE` original foram preservados.
