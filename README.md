# StoneStock

Sistema de controle de estoque em linha de comando (CLI), feito em Python, para pequenas empresas.

**Status:** em desenvolvimento (v0.1)

## Por que fiz

Quero aprender backend com Python construindo algo que se parece com um sistema real: regras de negócio, validação de dados, tratamento de erros e testes. O estoque de uma pequena loja é um problema simples de entender e rico em regras.

## O que já funciona

- [ ] Cadastrar produto (nome, preço e quantidade, com ID gerado automaticamente)
- [ ] Listar todos os produtos
- [ ] Buscar produto por ID
- [ ] Registrar entrada e saída de estoque
- [ ] Remover produto
- [ ] Salvar e carregar os dados em arquivo JSON
- [ ] Menu interativo no terminal

## Regras de negócio

- O preço deve ser maior que zero.
- A quantidade em estoque nunca fica negativa. Uma saída maior que o estoque é recusada.
- Não existem dois produtos com o mesmo nome (sem diferenciar maiúsculas de minúsculas).
- O ID não muda depois de criado.

## Tecnologias

- Python 3.11+
- pytest (testes)

## Como rodar

```bash
git clone https://github.com/ingridrenatadev-bit/StockStone.git
cd StockStone
python main.py
```

## Exemplo de uso

<!-- Coloque aqui um print ou GIF curto do terminal com o menu e uma operação. -->

## Estrutura do projeto

<!-- Ajuste para a estrutura real do seu projeto. -->

```
StockStone/
├── main.py            # menu e interação com o usuário
├── produto.py         # classe Produto (validações de preço e quantidade)
├── estoque_service.py # regras de negócio (cadastrar, buscar, atualizar, remover)
├── repositorio.py     # leitura e escrita do arquivo JSON
├── excecoes.py        # exceções do sistema
└── tests/             # testes com pytest
```

## Decisões de design

- **Camadas separadas:** a interface, as regras de negócio e a gravação em arquivo ficam em arquivos diferentes. Assim posso trocar o JSON por um banco de dados depois sem mexer nas regras.
- **Produtos em um dicionário com o ID como chave:** a busca por ID não precisa percorrer a lista inteira.
- **Exceções próprias** (produto não encontrado, estoque insuficiente, produto duplicado): cada erro tem nome e significado, em vez de uma mensagem genérica.
- **Operações parecidas com CRUD de API:** criar, ler, atualizar e remover seguem o mesmo desenho de uma API REST, para facilitar a migração para FastAPI.

## Testes

```bash
pytest
```

## Próximos passos

- [ ] v0.2: testes automatizados com pytest
- [ ] v0.3: API com FastAPI
- [ ] v0.4: banco de dados SQL (SQLite)
- [ ] v0.5: autenticação, senha com hash, validação de entrada e log de auditoria

## O que estou aprendendo

Programação orientada a objetos, encapsulamento, tratamento de exceções, persistência em arquivo e organização de projeto em camadas.

## Autora

Ingrid Renata Rodrigues
[LinkedIn](https://www.linkedin.com/in/ingrid-renatarodrigues-264286342) · [GitHub](https://github.com/ingridrenatadev-bit)
