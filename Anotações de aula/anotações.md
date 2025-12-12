#### Resumo da aula do dia 18/11
- inicio da matéria de Computação em nuvem 1;
- Descrever o que são Cliente e servidor: cliente (quem faz as requisições), API (meio que conecta o cliente com o servidor) e servidor (quem recebe e devolve as requisições);
- Definição de conceitos de nuvem: entrega sob demanda (só paga o que usar);
- Tipos de implementação de nuvem: On-premise (local), cloud (remoto) e hibrido (os 2 juntos);

---

#### Resumo da aula do dia 25/11
- Recaptulação dos temas passados na ultima aula;
- Maquinas virtuais e zonas de disponibilidade;
- Responsabilidade;
- um pouco sobre o SaaS;

---

#### Resumo da aula do dia 29/11 (Reposição de sábado)
##### Parte 1 - presencial:
- Responsabilidade compartilhada;
- Zonas de disponibilidade;
- criação de conta na Azure;
- inicio de exploração dentro da plataforma Azure;
- 
##### Parte 2 - Remoto:
- beneficios da nuvem - escalabilidade, disponibilidade, segurança...;
- criterios na criação de uma maquina virtual (região, hardware, colocar criptografia, IP...);
- prgramação para a P1 - revisar conteúdo até o slide 10;

---

#### Resumo da aula do dia 02/12
- Antes de criar uma VM, é recomendado criar uma rede virtual antes;
- Container = Caixa;
    - containers guardam MS (microserviços);
        - exemplo: container só pra mandar e-mail…
- Docker: gerenciador de containers;
- imagens podem existir sem container, mas um container n existe sem a imagem;

- Container Vs. VM Vs. Maquina física:
    - Container utiliza os recursos da maquina fisica, (isso permite que ele funcione em qualquer OS, pois ele só depende do Kernel);
    - Maquina fisica precisa do hardware;

- Tipo de serviço de nuvem:
    
    **IaaS (Infraestrutura como Serviço)**
    
    → Provedor cuida da infraestrutura física e virtual.
    
    → Cliente gerencia SO e aplicativos.
    
    **PaaS (Plataforma como Serviço)**
    
    → Provedor gerencia infraestrutura + sistema operacional + runtime + ferramentas.
    
    → Cliente apenas desenvolve e executa o código.
    
    **SaaS (Software como Serviço)**
    
    → Provedor entrega a aplicação pronta.
    
    → Cliente apenas usa; não configura nada técnico.
    

**Modelo de responsabilidade compatilhada:**

![alt text](image.png)

#### parte da aula foi um exercício sobre criar VMs

---

#### Resumo da aula do dia 06/12 (Reposição de sábado)
Parte 1:

- recaptulação:
    - IaaS, PaaS e SaaS (infraestruturas, plataformas e serviços);
        - IaaS: parte fisica, servidores…
        - PaaS: OS (ou VMs) e ferramentas para desenvolvedores, análise de negócios e gerenciamento de DB;
        - SaaS: serviços usados por alguém, como aplicativos e apps hospedados;
    - responsabilidade compartilhada;
    - casos de uso apropriado para cada serviço;
    
    - ipconfig: mostra os ips da maquina
    - Gateway: caminho por onde a conexão passa até encontrar o destino (pique um roteador)
    - DMZ: zona soberana: somente um pessoal especifico tem acesso
 
    Como fazer a VM q roda Windows:
    acessa o site:
    https://portal.azure.com/
    
    vai nas tres linhas, na parte de cima a esquerda e escolhe maquinas virtuais
    
    seleciona criar > maquina virtual
    
    basico:
    
    - assinatura: Azure for Students
    - grupo de recursos: cria um com qualquer nome
    - nome da maquina: qualquer um
    - região: geralmente eu escolho o Brazil south
    - imagem: windows server 2025 datacenter (não é o azure edition nem o core)
    - conta de adiministrador: nome do usuario: qualquer nome
    - senha: uma senha qaulquer (anota a senha e o nome de user, vai usar isso para acessar dps)
    
    Rede:
    
    - rede virtual: cria uma na hr ou usa uma existente
    
    Revisar + criar
    
    após criar, vc vai novamente nas maquinas virtuais, escolhe a maquina q vc criou e então liga ela (botão iniciar)
    
    após ligar, selecionar conectar por meio do bastion
    
    no bastion, seleciona a autenticação como senha do VM, coloca o nome do usuario e a senha anotados anteriormente e dps conectar
    
    permite pop-up no navegador para abrir a tela do bastion
    
    caso de erro, reinicia a Vm e repete a etapa de conectar
    
    se n der erro, ent tá pronto!

Parte 2:
- explicação de como fazer as VMs, escolha de zonas, regioes, como gerar arquivos RDP e como acessar as VMs remotamente.

#### Resumo da aula do dia 09/12 - 
`Faltei`

#### Resumo da aula do dia 12/12
`em andamento`