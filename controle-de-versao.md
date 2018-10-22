# Controle de Versão

## Conceito
 - Um sistema de controle de versão (ou versionamento), na função prática da ciência da computação ou da engenharia de software, é um software que tem como finalidade gerenciar diferentes versões no desenvolvimento de um documento qualquer.

## Funcionamento

- Nos sistemas de controle de versão (VCS) eles mantém registrado o que foi alterado, quando, quem, e porque foram alterados.
- Possuem também um histórico de mudanças.
- Permite também  voltar e avançar nas modificações, vendo diferentes estados e desfazer mudanças.
- As ferramentas previnem perda de informação
- Comparam diferentes estados o que ajuda na resolução de bugs.

![image](https://user-images.githubusercontent.com/18054053/47293719-4eba7300-d5e1-11e8-88cf-26be137c3231.png)
> Figura que exemplifica como os ramos (branches) trabalham em conjunto para mantes um versionamento mais organizado.


### Sistemas de controle de versão descentralizados

- Copias de trabalho, funcionam de um meio descentralizado, sem cópia central remota, cada um tem uma cópia.
- Possui um tipo de trava (Copia-Modifica-Resolve)
- Caso ocorram conflitos você irá resolver.
- Exemplos: Git, Mercurial, Bazaar.

- Vantagens - não requer ferramentas.
- Desvantagens - Maior complexidade em mesclar as modificações.


### Sistemas de controle de versão centralizados

- Cópia remota em algum servidos
- Todos podem saber quem está trabalhando no que.
- Mais poderes para o administrador como o controle de acesso

- Possuem travas do tipo (Trava-modifica-destrava), o que bloqueia acesso a um arquivo, não permite trabalhos parelolos, mas torna-se mais fácil de mesclar trabalhos

- Vantagens - fácil de compartilhar trabalho, não gera conflitos
- Desvantagens - Não há trabalho paralelo no mesmo arquivo

![image](https://user-images.githubusercontent.com/18054053/47295114-4ebc7200-d5e5-11e8-8db4-c3e22299e9ed.png)


## Git

- Sistema de controle de versão distribuído
- O sistema mais utilizado em projetos open-source
- Criado em 2005 por Linus Torvalds
- Substituto ao BitKeeper no projeto do Kernel do Linux
- Git foi desenhado para aplicar patch/diff em 3 segundos ou menos
- Segue um workflow perto do BitKeeper
- Suporte a desenvolvimento não linear (Milhares de Branches)
- Ser o oposto ao CVS (Concurrent Versions System)

### Repositório.
- Guarda arquivos
- Guarda configurações
- Guarda todas as versões
- Repositório remoto em um servidor, compartilhada entre vários desenvolvedores, facilita a comunicação, rastreio de bugs e funcionalidades.


### Fluxo de trabalho.

- Cria um fork do Repositório principal, clona o repositório para a máquina local, trabalha em modificações, manda para o teu fork e manda um Pull Request ou Merge Request para o repositório oficial. 
