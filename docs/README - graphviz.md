- [1. Uso do Graphviz com Poetry no Windows](#1-uso-do-graphviz-com-poetry-no-windows)
  - [1.1. ✅ 1. Instalação da biblioteca Python com Poetry](#11--1-instalação-da-biblioteca-python-com-poetry)
  - [1.2. ✅ 2. Instalação do executável Graphviz (binário do sistema)](#12--2-instalação-do-executável-graphviz-binário-do-sistema)
    - [1.2.1. Passos:](#121-passos)
  - [1.3. ✅ 3. Configuração do PATH no Windows](#13--3-configuração-do-path-no-windows)
  - [1.4. ✅ 4. Verificação da instalação](#14--4-verificação-da-instalação)
  - [1.5. ✅ 5. Teste em código Python](#15--5-teste-em-código-python)
  - [1.6. 🧠 Observações](#16--observações)
  - [1.7. 📁 Estrutura recomendada de projeto](#17--estrutura-recomendada-de-projeto)
  - [1.8. 📚 Referências](#18--referências)

# 1. Uso do Graphviz com Poetry no Windows

Este guia descreve como configurar e usar a biblioteca `graphviz` em um projeto Python gerenciado com [Poetry](https://python-poetry.org/) no sistema operacional **Windows**.

---

## 1.1. ✅ 1. Instalação da biblioteca Python com Poetry

Abra o terminal na raiz do seu projeto e execute:

```bash
poetry add graphviz@0.10
```

Isso adicionará a biblioteca `graphviz` como dependência do seu projeto.

---

## 1.2. ✅ 2. Instalação do executável Graphviz (binário do sistema)

A biblioteca Python depende do programa `dot` para gerar arquivos gráficos. Esse programa precisa estar instalado **separadamente** no sistema.

### 1.2.1. Passos:

1. Acesse: https://graphviz.gitlab.io/download/
2. Baixe o instalador `.exe` para Windows (exemplo: `graphviz-2.44.1-win64.exe`)
3. Instale normalmente.

---

## 1.3. ✅ 3. Configuração do PATH no Windows

Para que o Python encontre o `dot.exe`, é necessário adicionar o Graphviz ao PATH do sistema:

1. Vá em:
   ```
   Painel de Controle → Sistema → Configurações Avançadas → Variáveis de Ambiente
   ```
2. Em "Variáveis do Sistema", localize a variável `Path` e clique em "Editar".
3. Adicione o seguinte caminho (ajuste conforme sua instalação):

   ```
   C:\Program Files\Graphviz\bin
   ```

4. Clique em OK e **reinicie o terminal** para que as mudanças tenham efeito.

---

## 1.4. ✅ 4. Verificação da instalação

Abra um novo terminal e execute:

```bash
dot -V
```

Você deve ver algo como:

```
dot - graphviz version 2.44.1 (20200629.0846)
```

---

## 1.5. ✅ 5. Teste em código Python

```python
from graphviz import Digraph

dot = Digraph()
dot.node('A')
dot.node('B')
dot.edge('A', 'B', label='A para B')

dot.render('meu_grafo', format='png', cleanup=True)
```

Esse código irá gerar um arquivo `meu_grafo.png` com o grafo desenhado.

---

## 1.6. 🧠 Observações

- Se `dot` não for encontrado, verifique se o caminho está corretamente configurado no `PATH`.
- A biblioteca Python `graphviz` não funciona sozinha — ela apenas gera comandos para o programa `dot`, que é quem realmente desenha os gráficos.

---

## 1.7. 📁 Estrutura recomendada de projeto

```
meu-projeto/
│
├── README.md
├── pyproject.toml
├── poetry.lock
├── main.py
└── meu_grafo.png  # Saída do render()
```

---

## 1.8. 📚 Referências

- [Documentação oficial do Graphviz (Python)](https://graphviz.readthedocs.io/)
- [Site oficial do Graphviz](https://graphviz.org/)
- [Poetry](https://python-poetry.org/)
