# Explorando Práticas de Teste

Neste exercício, vamos explorar práticas de teste em sistemas reais utilizando a ferramenta [TestMiner](https://andrehora.github.io/testminer).

O TestMiner permite visualizar e analisar testes de software em repositórios do GitHub, fornecendo dados sobre como os projetos organizam seus testes, como eles evoluem entre versões e quais bibliotecas de teste são utilizadas.
Explore a ferramenta antes de começar para se familiarizar com seu funcionamento.

---

## Passo 1: Selecionar um repositório

Escolha um repositório real que possua testes escritos na linguagem de sua preferência.
Abaixo estão alguns links para ajudá-lo a encontrar projetos interessantes:

- **Python:** https://github.com/topics/python?l=python
- **JavaScript:** https://github.com/topics/javascript?l=javascript
- **TypeScript:** https://github.com/topics/typescript?l=typescript
- **Java:** https://github.com/topics/java?l=java

## Passo 2: Explorar o repositório selecionado

Busque o repositório escolhido no [TestMiner](https://andrehora.github.io/testminer) e analise os dados de teste gerados pela ferramenta.

## Passo 3: Explicar uma prática de teste

Com base nos dados obtidos, selecione uma prática ou dado de teste relevante e explique-o com suas próprias palavras.

---

## Instruções de entrega

1. Faça um `fork` deste repositório (saiba mais sobre forks [aqui](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo)).
2. Responda às questões abaixo diretamente neste arquivo `README.md` do seu fork. Pode adicionar imagens para enriquecer sua explicação.
3. No Moodle, submeta apenas a URL do seu fork.

---

## Respostas

**1. Repositório selecionado:** https://github.com/pandas-dev/pandas`

**2. Explicação:** O repositório Pandas foi selecionado para essa analise devido ao uso amplamente difundido dessa biblioteca entre programadores. Uma prática relevante observada nos dados é o uso de mocks, tendo apenas 3 ocorrências apontadas pelo TestMiner. Em geral, mocks são usados para substituir dependências externas ou partes complexas do sistema durante os testes, permitindo isolar comportamentos específicos. No entanto, o que o TestMiner apontou como mocks contém na verdade fixtures do pytest, que tem como objetivo fornecer dados reutilizáveis para os testes. Essas fixtures, como dummies_basic e dummies_with_unassigned, simulam diferentes cenários de entrada para a função from_dummies.
O principal objetivo é testar o comportamento da função from_dummies, especialmente em situações de erro e condições de borda.
Por exemplo:

•	Tipos de entrada inválidos 
•	Dados inconsistentes (NaN, valores inválidos) 
•	Casos de uso reais 
•	Compatibilidade com diferentes tipos de dados (int, float, string, bool)

Isso permite verificar se a transformação de variáveis dummy em categorias ocorre corretamente e se erros corretos são lançados quando necessário. Assim, o foco está em garantir robustez e confiabilidade por meio de dados bem definidos, através do uso de fixtures.

