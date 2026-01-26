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

- 
---

#### Resumo da aula do dia 09/12
`Faltei`

---

#### Resumo da aula do dia 12/12
Maquinas Virtuais:

- VMs: emulações de software de computadores fisicos
- fluxograma de relação entre computadores e maquinas virtuais: PC → ( OS → Kernel ) → VMs
- conjunto de disponibilidade de VM:

- Racks: amontoados de nuvem em uma prateleira (geralmente tendem a dar problema algum dia)
    - geralmente há sempre 3 racks por zona.
- Area de trabalho virtual: versão remota de uma area de trabalho do desktop
- Containeres: ambiente leve e virtualizado que não exigem gerenciamento de sistema
- instancia de containers: oferta de PaaS que executa um container ou pod (um monte de containers).
- aplicativos de container: oferta de PaaS, como instancias de containers, que balancear carga e escalar
- serviço de Kubernetes: serviços de orquestração de containers
    - uma imagem pode ter varios containers, porem os containers podem ter apenas uma imagem (1 → n)
    - a necessidade de se ter muitos containers é devido aos microserviços (rodar serviços em containers separados), isso impede um sistema de parar por completo, sendo agora apenas por pedaços

- Azure Functions: oferta do PaaS, dá suporte a operações de computação sem servidor (msm coisa de função, se usa quando chama ela)

- comparação de opções de computação:
    - VMs:
        - suporte a ambientes Windows e Linux;
        - migrações lift-and-shift (**Rehospedagem**) para a nuvem;
    - Area de trabalho Virtual:
        - experiencia da area de trabalho windows baseada em nuvem (RDP);
        - apps dedicados para conexão e uso (SaaS);
        - multiplos logons que podem ser usados ao msm tempo (recomendado no max 10 usuarios, senão deixa mais lento);
    - Containers:
        - ambiente leve e em miniatura para rodar microserviços;
        - projetados para serem escalaveis e resilientes por meio da orquestração;
        - os apps são empacotados no container q fica na parte superior do OS.
        - Varios containers podem ficar em um OS

- serviços de aplicativos do Azure: plataforma gerenciada para criar, implementar e dimensionar aplicativos web e APIs rapidamente.
    - trabalha com multiplas linguagens (java, net, PHP e outros)

- sub-redes virtuais: segmentam a rede atendem suas necessidades;
- as redes privadas são conectadas diretamente via **emparelhamento de redes**;
- Gateway de VPN: usado para enviar trafego criptografado entre uma rede virtual e uma rede local pela internet publica;
- ExpressRoute: estende as redes locais por meio de uma conexão privada facilitada por um provedor de conectividade;
- DNS do azure: pega um dominio e direciona a um IP (é tipo identificar uma pessoa através do CPF dela)
    - monitora e gerencia os logs
    - 192.0.0.1 → IP do localhost
    - alias: nomes para o IP (ou apelidos)

final da aula foi visualização leve da azure functions

---

#### Resumo da aula do dia 15/12
Revisão pré P1:

- Cadeia cliente-servidor

![image.png](attachment:501f5715-ced2-44b2-929f-dae98ce64140:image.png)

1. cliente
2. cliente
3. cliente e servidor
4. servidor e micro-serviço
- a importância de se definir 3 servidores, é para evitar sobrecarga e dividir tarefas

- descrever Iaas, Paas e Saas:
    - IaaS: infraestrutura (parte fisica, servidor…)
    - PaaS: plataforma (OS e ferramentas)
    - SaaS: software (só pegar e usar, app online e/ou software)

- descrever o modelo de reponsabilidade compartilhada (baseado naquele grafico dos quadradin)

- resolver essas questões para estudar e mandar pro git:

![image.png](attachment:44af37f1-b0f9-4e50-baf1-57fbed0b1adb:image.png)

entregaveis:

- prints dos links acima (os quizzes)
- os RDPs, logins e senhas
- link do github

---

#### Resumo da aula do dia 18/12
- apresentação da P2
