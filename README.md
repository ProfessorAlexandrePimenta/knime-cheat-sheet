# KNIME Cheat Sheet

Página responsiva de consulta rápida do KNIME Analytics Platform, em português, com interface glassmorphism.

## Funcionalidades

- 105 fichas de consulta em 12 categorias.
- Busca por nome, tarefa ou conceito, com suporte a termos sem acentos.
- Filtros por categoria e ordenação alfabética.
- Temas claro e escuro, com preferência salva no navegador.
- Favoritos locais, fichas detalhadas e impressão da seleção.
- 8 receitas de workflows e exemplos copiáveis de Rule Engine, Math Formula, Python e SQL.
- Links para a documentação oficial e o KNIME Community Hub.

## Acessar

Site: https://knime-cheat-sheet-pimenta.free-goose-4783.chatgpt.site

O acesso ao site no Sites depende das configurações de compartilhamento do proprietário. Este repositório contém uma cópia independente do código.

## Executar localmente

Não há dependências de build. Com Python 3 instalado, execute na pasta do projeto:

```bash
python -m http.server 8000 --directory dist
```

Abra http://localhost:8000 no navegador. Favoritos e tema são salvos com localStorage; a cópia automática depende das permissões do navegador e de um contexto seguro.

## Estrutura

| Arquivo | Função |
| --- | --- |
| dist/index.html | Estrutura, estilos e layout responsivo |
| dist/app.js | Busca, filtros, tema, favoritos e diálogos |
| dist/data.js | Conteúdo das 105 fichas |
| make.py | Gerador do conteúdo de dist/data.js |
| check.cjs | Verificações funcionais em ambiente simulado |

## Editar o conteúdo

Edite as fichas em `make.py` e execute `python make.py` na raiz do projeto. O gerador sobrescreve `dist/data.js`. Para mudar o visual, edite `dist/index.html`; para mudar interações, edite `dist/app.js`.

## Verificar

Com Node.js instalado:

```bash
node --check dist/app.js
node --check dist/data.js
node check.cjs
```

As verificações cobrem busca, estado vazio, favoritos, diálogo e troca de tema com DOM simulado; não substituem revisão visual em navegador.

## Hospedar

Publique o conteúdo de `dist/` em qualquer hospedagem de arquivos estáticos. Para GitHub Pages, use `dist/` como artefato de uma implantação por Actions ou copie seu conteúdo para a pasta configurada no Pages. A publicação no GitHub Pages não é ativada automaticamente por este envio.

## Referências

- [Guia oficial do KNIME](https://docs.knime.com/ap/latest/analytics_platform_user_guide/)
- [KNIME Community Hub](https://hub.knime.com/)
- [IA no KNIME](https://docs.knime.com/ap/latest/ai/overview/)
- [Integração Python](https://docs.knime.com/ap/latest/python_installation_guide/)
- [Cuidados com a divisão de treino e teste](https://www.knime.com/blog/3-must-avoid-pitfalls-splitting-datasets-train-test-data)

Referências consultadas em 06/10/2026. Guia educacional independente: nomes de nós, interfaces e extensões podem variar por versão. KNIME é marca de seus respectivos titulares.

Fontes DM Sans e Space Grotesk são carregadas pelo Google Fonts, com fontes locais alternativas quando indisponíveis. Nenhuma credencial ou configuração privada do Sites integra este repositório.
