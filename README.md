# Arquitetura de software

## Fundamentos

### Tipos de arquitetura
- Software;
- Solução;
- Tecnológica;
- Corporativa.

#### Software
- É uma "disciplina" da engenharia de software;
- Diretamente ligada ao processo de desenvolvimento de software. Arquitetura de software é mais baixo nível do que arquitetura de solução;
- Afeta diretamente na estrutura organizacional da empresa, como por exemplo:
    - Formação dos times;
    - Estrutura dos componentes do software;
    - Lei de Conway: "Organizações que desenvolvem sistemas de software tendem a produzir sistemas que são cópias das estruturas de comunicação dessas empresas. "Melvin Conway".

Se pudessemos definir a arquitetura de software, seria: **a relação entre os objetivos de negócios e suas restrições com os componentes a serem criados e suas responsabilidades visando sua evolução do software.**

A definição mais formal é dada por: "É a organização fundamental de um sistema e seus componentes, suas relações, seu ambiente, **bem como os princípios que guiam seu design e evolução**." (IEEE Standard 1471)

O processo de arquitetar um software estabelece que o que está sendo desenvolvido faça parte de um conjunto maior.

#### Tecnológica
- Focado em **especialidade em tecnologias específicas de mercado**;
- O arquiteto vai **geração de valor baseado em especialidades**.

Exemplo de arquitetos tecnológicos:
- Arquiteto Elastic
- Arquiteto Java
- SQL Server
- Oracle
- SAP

#### Solução
- Fica entre a área de negócios e software, portanto é uma área técnica com visão no negócio;
- Transforma requisitos de negócios em soluções de software;
- Desenhos arquiteturais da solução de um software para reproduzir como ele irá funcionar. Por exemplo:
    - C4;
    - UML;
    - BPMN.
- Analisa os impactos comerciais em relação a uma escolha de tecnológica;
- Pode participar do processo comercial de pré-venda e venda;
- Analisa os impactos dos custos para o negócio.

#### Corporativa
- **Politicas e regras** que impactam estrategicamente a organização como um todo;
- Arquitetura corporativa consegue fazer uma **avalição de custos** que toda a area de engenharia e de desenvolvimento vai ter para poder desenvolver os projetos para fazer a empresa crescer;
- **Avaliação de possíveis novas tecnologias**;
- **Padronização de tecnologias**;
- **Planejamento de grandes implantações**.

Exemplo de arquitetos corporativos:
- Sistema "core";
- Migrações.

### Papel do arquiteto de de software
- Transformar requisitos de negócios em padrões arquiteturais;
- Orquestrar pessoas desenvolvedores e experts de domínio;
- Entender de forma profunda conceitos e modelos arquiteturais;
- Auxilia na tomada de decisão nos momentos de crise;
- Reforça boas práticas de desenvolvimento;
- Code reviews;
- Apesar de nem todas as organicações possuírem o cargo de arquiteto de software, normalmente profissionais mais experientes como desenvolvedores seniors e tech leads acabam realizando esse papel baseado em suas experiencias anteriores;
- Há empresas que apesar de não possuírem o cargo de arquiteto de software, possuem um departamento de arquitetura que auxilia os diversos times da organização com questões arquiteturais;
- **OBS: [Manual do Arquiteto de Software](https://arquiteturadesoftware.online/).**

### Por que aprender arquitetura de software?
- Pode navegar da visão macro para a visão micro de um ou mais softwares;
- Entender quais são as diversas opções que temos para desenvolver a mesma coisa e escolher a melhor solução para determinado contexto;
- Pensar a longo prazo no projeto e sua sustentabilidade;
- Tomar decisões de forma mais fria e calculada evitando assim ser influenciado(a) por "hypes" de mercado;
- Mergulho em padrões de projeto e de desenvolvimento e suas boas práticas;
- Ter mais clareza do impacto que o software possui na organização como um todo;
- Tomar decisões com mais confiança.

### Arquitetura vs Design de software
- Arquitetura: Escopo global ou alto nível;
- Desgin de software: Escopo local;
- "Atividades relacionadas a arquitura de software são sempre de design. Entretanto, nem todas atividades de desgin são sobre arquitetura. O objetivo primário da arquitetura de software é garantir que os atributos de qualidade, restrições de alto nível e os objetivos do negócio, sejam atendidos pelo sistema. Qualquer decisão de design que não tenha relação com este objetivo não é arquitetural. Todas as decisões de design para um componente que não sejam "visíveis" fora dele, geralmente, também não são." - "Elemar Jr".

### Sustentabilidade
- Desenvolver software é caro;
- Software resolve uma "dor";
- Software precisa se pagar ao longo do tempo;
- Acompanhar a evolução do negócio;
- Quanto mais tempo o software fica no ar, mais retorno gera;
- A solução precisa ser arquitetada.

### Pilares da arquitetura de software
- Estruturação:
    - Fácil evolução, componentização para entender os objetivos de negócio.
- Componentização;
- Relacionamento entre sistemas;
- Governança.

### Requisitos arquiteturais (RAs)
- Performance;
- Armazenamento de dados;
- Escalabilidade;
- Segurança;
- Legal;
- Audit;
- Marketing.

## Características arquiteturais
- Operacionais;
- Estruturais;
- Cross-Cutting;
- OBS: Esses itens foram tirados do livro - Fundamentos de arquiteturas de software.

#### Características arquiteturais: Operacionais
- Disponibilidade;
- Recuperação de desastres;
- Performance;
- Recuperação (backup);
- Confiabilidade e segurança;
- Robustez;
- Escalabilidade:
    - Verticalmente: aumenta o recurso computacional de uma máquina;
    - Horizontalmente: adiciona mais máquina.

#### Características arquiteturais: Estruturais
- Configurável;
- Extensibilidade;
- Fácil intalação: 
    - hoje em dia o modo mais simples é utilizando containers;
- Reuso de componentes;
- Internacionalização:
    - tanto do backend (e.g. moedas) quanto do frontend (e.g. idiomas)
- Fácil manutenção:
    - quanto mais simples o software ficar, mais fácil será a manutenção;
    - utilizar sempre o SOLID;
    - usar adapters;
    - trabalhar sempre com testes;
- Portabilidade (diversos bancos de dados):
    - sistemas menos dependentes dos vendors
- Fácil suporte:
    - Logs;
    - debugging

#### Características arquiteturais: Cross-Cutting
- Acessibilidade:
    - Ter ciencia do público que vai acessar sua aplicação
- Processo de retenção e recuperação de dados (quanto tempo os dados serão mantidos)
    - Dados quentes: que são utilizados toda hora. Pode ser guardado em ambientes que permite acesso frequente,
    - Dados frios: guardar de forma compactada, pois não serão acessados frequentemente.
- Autenticação e Autorização:
    - API Gateway: mecanismo utilizado na borda da aplicação. Quando o usuário acessa sua aplicação ele bate lá primeiro. Pode utilizar diversos plugins, tais como:
        - Politicas de autenticação, politicas de time out, politica de quantidade de requisição
- Legal:
    - Tudo que acontece na sua aplicação tem que estar em conformidade com as leis do pais onde ele estiver rodando.
- Privacidade:
    - Como conseguir minimizar problemas de dados de usuários que podem vazar.
- Segurança:
    - De ponta a ponta, dês da borda;
    - Trabalhe com WEB firewall;
    - Utilize ao máximo tudo que é padrão aberto.
- Usabilidade:
    - No frontend existem diversas ferramentas que facilitam enxergar a usabilidade do usuário;
    - No backend, a API precisa ter:
        - documentação;
        - fácil utilização; 
        - trabalhar sempre com padrões como a Open API;
        - contrato claro com a API;
        - ter um bom README.

## Perspectivas para arquitetar software de qualidade
- Performance;
- Escalabilidade;
- Resiliência;

### Performance
- É o desempenho que um software possui para completar um determinado workload;
    - Faz comparação entre versões do software ao longo do tempo.
- As unidades de medida para avaliarmos a performance de um software são:
    - Latência ou "response time": tempo de efetuar uma requisição, processar a chamada e retornar o resultado.
    - Throughput: mostra o quanto de requisão o software consegue aguentar.
- Ter um software performático é diferente de ter um software escalável

#### Métricas para medir a performance
- Diminuindo a latência:
    - Normalmente medida em miliseconds. Caso a requisição passe a ser medida em segundos, já é considerada inaceitavel.
    - É afetada pelo tempo de processamento da aplicação, rede e chamadas externas. Quanto mais longe estiver do datacenter, pior vai ser.
- Aumentando o throughput:
    - Permitindo aumento de quantidade de requisições.
    - Diretamente ligado a latência. Quanto mais requisição presa estiver na aplicação, esperando a resposta, acaba diminui o throughput.

#### Principais razões para baixa performance
- Processo ineficiente: 
    - Quanto se tem um sistema que esta trabalhando de forma ineficiente, gera baixa performance.
- Recursos computacionais limitados:
    - Quanto maior seu hardware, maior seu custo. E quanto menor seu hardware, menor seu custo.
- Trabalhar de forma bloqueante:
    - Efetuar o processamento de requisições não bloqueantes. Vai gerar um poder maior de performance.
- Acesso serial a recursos:
    - Cada vez que vai acessar uma API e espera terminar e depois vem a próxima requisão, ou seja, trabalhando de forma serial. Isso vai causar uma redução do throughput.

#### Principais razões para aumentar a eficiência da performance
- Escala da capacidade computacional (CPU, Disco, Memória, Rede);
- Lógica por trás do software (Algoritmos, queries, overhead de frameworks);
- Concorrência e paralelismo;
- Banco de dados (tipos de bancos, schema);
- Caching.

#### Capacidade computacional: Escala vertical vs horizontal
- Escala vertical: aumentar os recursos computacionais.
- Escala horizontal: aumento a capacidade de máquinas ativas. Em conjunto com um load balancer para gerenciar a carga.

#### Diferença entre concorrência e paralelismo
- "Concorrência é sobre lidar com muitas coisas ao mesmo tempo. Paralelismo é fazer muitas coisas ao mesmo tempo." - Rob Pike.

#### Caching
- Cache na borda / Edge computing:
    - Esse tipo de cache faz com que o usuário nem bate na sua cloud, pois esse cache traz pontos totalmente processados em um servidor que fica antes do seu servidor principal.
    - Por exemplo uso de Cloudflare. E não tem um custo alto, comparado aos custos de infra.
- Dados estáticos:
    - Comum querer cachear CSS, HTML e imagens por exemplo.
    - Muito barato;
- Páginas web:
- Funções internas:
    - Evita reprocessamento de algoritmos pesados
    - Acesso ao bacon de dados. Acessar banco de dados é extremamente caro e custoso.
- Objetos
    - Existem objetos que o seu sistema vai ter que ficar criando o tempo inteiro para gerar processamento de alguma forma.

#### Caching: Exclusivo vs Compartilhado
- Exclusivo: cache que funciona de forma local
    - Baixa latência
    - Duplicado entre os nós
    - Problemas relacionados a sessões
- Compartilhdo: cache esta centralizado
    - Maior latência;
    - Não há duplicação;
    - Sessões compartilhadas;
    - Banco de dados externo: podendo cachear os dados nesse banco
        - MySQL
        - Redis
        - Memchache

#### Caching: Edge computing
- A internet não consegue mais funcionar sem o Edge computing, como por exemplo a Netflix. Sem o Edge computing a quantidade de trafego que a Netflix precisaria para funcionar iria causar sobrecarga a internet de forma geral.
- Consegue fornecer serviços além da CDN, que consegue processar informações mais proximas do usuários evitando com que essa informação bata no seu servidor.
- Cache realizado mais próximo ao usuário;
- Evita a requisição chegar até o Cloud Provider / Infra;
- Normalmente arquivos estáticos;
- CDN - Content Delivery Network (Akamai);
- Cloudflare workers: permite que faça deploy de aplicações que serão executadas em JS. Pois eles conseguiram isolar (mini container) cada chamada utilizando a engine V8 (node, google, browser) e que conseguem ser executada de forma rápida e mais próxima ao usuário.
- Vercel: empresa que mantém o NextJs.
- Akamai.

### Escalabilidade
- Escalabilidade é a capacidade de sistemas suportarem o aumento (ou a redução) dos workloads incrementando (ou reduzindo) o custo em menor ou igual proporção.

#### Escalabilidade vs Performance
- Enquanto performance tem o foco em reduzir a latência e aumentar o throughput, a escalabilidade visa termos a **possibilidade** de aumentar ou diminuir o throughput adicionando ou removendo a capacidade computacional.

#### Escalando software
- Escala vertical: aumentando o poder computacional
    - O problema da escala vertical é o limite do poder computacional da máquina. Um hora esse limite é alcançado. Além de centralizar todo o sistema em uma única máquina.
- Escala horizontal: aumentar a quantidade de máquinas
    - A vantagem da horizontal é que o sistema fica distribuido em várias máquinas e se uma der problema, nem todas ficarão fora do ar.
    - É a mais comum; 
    - O software terá que estar preparado para utilizar a escala horizontal.
- Quanto maior a escala (vertical/horizontal), maior a escala

#### Escalando software - Descentralização
- Disco efêmero: tudo que salvar em disco na máquina possa ser apagado quando necessário. Mudar para o uso de disco efêmero significa uma mudança de paradigma. A única utilização do disco é para arquivos temporários;
- Servidor de aplicação vs Servidor de assets;
- Cache centralizado;
- Sessões centralizadas;
- Upload / Gravção de arquivos: não ficam nas máquinas. Ficam em servidores de arquivos.

#### Escala de banco de dados
- Aumentando recuros computacionais: mais memória, disco melhor, processador melhor, etc;
- Distribuindo responsabilidades (escrita vs leitura);
- Shards de forma horizontal;
- Serverless: delega a responsabilidade do servidor para os cloud providers;

#### Otimização de queries e índices
- Tenha um sistema APM (Application Performance Monitor), com ele conseguimos entender todas as queries que estão rodando e enxergar os gargalos no banco de dados. Com APM nos conseguimos dar um **explain**, mostrando passo-a-passo a query rodando e ver o ponto que esta lento;
- Trabalhar com índices de forma consciente;
- CQRS (Command Query Responsibility Segregation): separação de leitura e escrita. Comando, que é uma inteção do usuário para gravação e a Query que é para fazer a leitura dos dados.

#### Proxy reverso
- Proxy reverso é um servidor que fica na frente dos servidores web e encaminha as solicitações do cliente (por exemplo, navegador web) para esses servidores web.

#### Soluções populares com proxy reverso
- Nginx
- HAProxy (HA = High Availability)
- Traefik

### Resiliência
- Resiliência é um conjunto de estratégias adotadas **intencionalmente** para **adaptação** de um sistema quando uma falha ocorre.
- Ter estratégias de resiliência nos possibilita **minimizar** os riscos de perda de dados e transações importantes para o negócio.

### Quais as estratégias?

#### Proteger e ser Protegido
- Um sistema em uma arquitetura distribuída precisa adotar mecanismos de autopreservação para garantir ao máximo sua operação com **qualidade**.
    - uma forma simples é retornar 500 quando perceber que o sistema está ficando sobrecarregado.
- Um sistema não poder ser "egoísta" ao ponto de realizar mais requisições em um sistema que está falhando.
- Um sistema lento no ar muitas vezes é pior do que um sistema fora do ar (efeito dominó).

##### Health check
- Sem sinais vitais, não é possível saber a "saúde" de um sistema;
- Um sistema que não está saudável possui uma chance de se recuperar caso o tráfego pare de ser direcionado a ele temporariamente. Esse processo de recuperação do sistema é chamado de **self healing**;
- Health check de qualidade
    - A qualidade do sistema não deve ser medida apenas por um arquivo HTML;
    - Deve usar de maneira estratégica, os dados necessários se acessados devem retornar 200, mas que ele consulte banco e efetuou verificações que indicam que o sistema está saudável.

##### Rate Limiting
- Proteger o sistema baseado no que ele foi projetado para suportar
    - É preciso saber o limite que o sistema aguenta
- Preferência programada por tipo de client, ou seja, colocar um limite específico por cada cliente.

##### Circuit breaker
- Protege o sistema fazendo com que as requisições feitas para ele sejam negadas. Ex: 500.
- Quando um sistema (A) estiver ficando sobrecarregado ele pode **abrir o circuito** a comunicação com outro sistema (B) até que ele comece a se recuperar e volte a funcionar normalmente **fechando o circuito** novamente;
- Circuito fechado = Requisições chegam normalmente
- Circuito aberto = Requisições não chegam ao sistema. Erro instantâneo ao client
- Meio aberto = Permite uma quantidade limitada de requisições para verificação se o sistema tem condições de voltar ao ar integralmente.
- Existem bibliotecas que fazem esse tipo de funcionalidade. Porém hoje em dia existe recursos mais modernos, e o circuit breaker é implementado diretamente na rede.

##### API Gateway
- Centraliza o recebimento de todas as requisições que estão acontecendo na sua aplicação.
- Garante que requisições "inapropriadas" cheguem até o sistema: Ex: usuário não autenticado.
- Implementa políticas de Rate Limiting, Health check, etc
- Ex: Kong

##### Service Mesh
- Conhecida como Malha de serviços;
- Controla o tráfego de rede
    - Permite colocar proxys do lado de cada sistema nosso, e toda a comunicação passa a ser intermediada por esses proxys antes de bater de fato no sistema desejado. Com isso tudo que passa pela rede passa a ser medido, controlado, obtenção de dados, informação.
- Evita implementações de proteção pelo próprio sistema
- Ajuda a controla tudo e entender o que ta acontecendo dentro da nossa rede;
- mTLS
- Permite trabalhar com Circuit breaker, retry, timeout, fault injection, etc.

##### Trabalhar de forma assíncrona
- Evita perda de dados
- Não há perda de dados no envio de uma transação se o server estiver fora
- O servidor pode processar a transação em seu tempo quando estiver online
- Entender com profundidade o message broker / sistema de stream