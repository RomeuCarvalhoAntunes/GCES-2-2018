# Integração contínua

## Conceito:
- Integração frequente das diferentes branches de trabalho.
> A integração contínua é uma prática de desenvolvimento de software de DevOps em que os desenvolvedores, com frequência, juntam suas alterações de código em um repositório central. Depois disso, criações e testes são executados. Geralmente, a integração contínua se refere ao estágio de criação ou integração do processo de lançamento de software, além de originar um componente de automação (ex.: uma CI ou serviço de criação) e um componente cultural (ex.: aprender a integrar com frequência). Os principais objetivos da integração contínua são encontrar e investigar bugs mais rapidamente, melhorar a qualidade do software e reduzir o tempo que leva para validar e lançar novas atualizações de software.

![image](https://user-images.githubusercontent.com/18054053/47299948-bed0f500-d5f1-11e8-9c7c-19c7ae66e2f1.png)

- A CI facilita praticas do XP (eXtreme Programming) entre eles estão os testes automatizados (TDD, Testes unitários, Testes de Integração), build automatizada (Build testável, Build Contínua), aumenta a frequência , rodando varias vezes ao dia a cada atualização de commit (testes e build).


### Benefícios e boas práticas
- Build Automática
- Build Testável
- Commits diários na master
- Commits testados e funcionando na master
- Build rápida
- Deploy Automático


### Integração Contínua != de Deploy Contínuo.

#### Conceitos gerais
- Deploy contínuo é a entrega contínua em produção para o cliente.
- Entrega contínua (Continuous Delivery) é diferente do deploy contínuo, a entrega contínua é: A habilidade de gerar uma build estável a qualquer momento
![image](https://user-images.githubusercontent.com/18054053/47300375-ac0af000-d5f2-11e8-80c8-ae79f2f0011c.png)


### Ferramentas que permitem a CI:
![image](https://user-images.githubusercontent.com/18054053/47300432-cfce3600-d5f2-11e8-9a6e-6a5905188053.png)

#### Ciclo do Travis.

- 1 Cria-se um arquivo .yml --> YAML que é parecido com o shell.
- 2 **apt addons** exclusivo do ubuntu, adiciona dependências e pacotes que serão usados dentro da máquina virtual do travis
- 3 **Cache components** --> responsável por marcar o que deve ser salvo após a build para evitar downloads lentos durante a build.
- 4 **Before install** --> comandos que devem ser executados antes da instalação do ambiente, possível para todos os sistemas operacionais.
- 5 **Install** responsável por instalar as dependências do projeto.
- 6 **Before Script** responsável por preparar o ambiente para o script.
- 7 **Script** responsável por executar build, testes e etc.
> caso a build falhe até o ponto 6 é o erro na build, no processo de build, caso ocorra erro no passo 7 é uma falha de build podendo ser por testes, builds etc etc.

- 8 **Before Cache** acontece antes de salvar o cache.
- 9 **After success/After failure** acontecem após a build dizendo se a build passou ou não, isto inclui todos os testes e estágios de build.
- 10 A integração contínua pode ser configurada junto com a entrega continua para possibilitar um deploy contínuo.
