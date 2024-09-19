# resumoLab

#Resumo de Aprendizado DIO.

#Capitulo 1;
  #Módulo Conceitos iniciais de Cloud com Azure.

  #Localizando serviço por categoria;
  
    Introdução de como localizar o tipo de serviço necessário;
    Familiarização com o ambiente de nuvem Azure;

  #Beneficios da computação em nuvem;
    #Alta Disponibilidade (SLA);
    
      Sistema com recursos necessários sempre disponiveis;
      Garantia de disponibilidade, modelos SLA 99%, 99.9, 99.95%, etc;
      SLA (Service Level Agreement);
      Caso a indisponibilidade passe o tempo de SLA ira ocorrer um ganho de crédito para uso futuro na plataforma;
  
    Escalabilidade;
      Alta capacidade de ajustar recursos para atender as demandas necessarias;
      Posso desprender mais recursos para lidar melhor com o aumento de demanda;
      Não paga alem do necessário;
  
    Elasticidade;
      Caso haja um aumento repentino na demanda, seus recursos podem ser expandidos automaticamente ou manualmente;
      Também é possivel reduzir os recursos;
  
    Confiabilidade;
      Devido a descentralização, a nuvem da suporte confiavel e resiliente;
      A nuvem permite ter recursos em diversas regiôes do mundo;
  
    Previsibilidade;
      Permite avançar com confiança, sem ser supreendido com desempenho ou custo;
      Influenciado pelo Microsoft Azure Well-Architected Framework;
  
    Segurança;
      Existem ferramentas que atendem às necessidades do cliente;
      Implementação é responsabilidade do cliente da nuvem;
      É possivel implementar patchs e manutenção de forma automatica;
  
    Governança;
      A auditoria baseada em nuvem ajuda a sinalizar qualquer recurso que esteja fora de conformidade ecom seus              padrões corporativos e oferece estratégias de mitigação;
  
    Gerenciabilidade;
      Capacidade de gestão alta;
      Liberdade de criação de recursos pelo portal Azure, powershell, linha de código, etc...;
      Implementação de recursos com base em modelos pré-configurados;
  
  
  #Tipos de serviços de nuvem;
  
    IaaS (Infraestrucura como Serviço);
      Maior gestão;
      Maior controle;
      Recursos dos quais o usuário se envolve mais;
  
    PaaS (Plataforma como Serviço);
      Gestão intermediaria;
      Controle moderado;
      Fornecimento de ambiente para criação, teste e implantação de aplicativo de software sem foco em gestão de             infraestrutura;
  
    SaaS (Software como Serviço);
      Menor gestão;
      Menor controle da aplicação;
      Uso direto, responsabilidades são de quem oferece o Software;
      Exemplos: Microsoft Office 365;

#Capitulo 2;
  #Arquitetura e Serviços Azure;
    
  #Componentes de Arquitetura do Azure;
  
      Regiões;
        Quando vamos criar um recurso é necessário escolher em qual região ele sera colocado;
        É necessário visualizar onde o seu recurso irá melhor se encaixar;
        É preciso estudar também onde será colocado o seu recurso para evitar delay caso seja necessário um recurso            sem delay;
        Azure conta com mais de 60 regiões representando mais de 140 paises;
        As regiões são compostas de um ou mais datacenter muito próximos;
        Eles fornecem flexibilidade e escala para dreduzir a latência do cliente;
        As regiões preservam a residência dos dados com uma oferta abrangente de conformidade;
          É necessário verificar o LGPD;
        Regiões são formadas por um conjunto de Datacenters;
        Ideal criação de um modelo de Desaster Recovery, utilizar outros DC's com o mesmo sistema que fica passivo             para que não seja perdida a funcionalidade caso aconteça um desastre;

  #Pares de Regiões;
  
      No mínimo 300 milhas de separação entre pares de regiões;
      Replicação automática para alguns serviços;
      Recuperação de região priorizada em caso de interrupção;

  #Regiões soberanas do Azure;
  
      Serviços Governamentais dos EUA;
        Atende às necessidades de segurança e conformidade das agências federais, governos estaduais e locais dos EUA e seus provedores de soluções;
        Azure Governamental;
          Instância separada do Azure;
          Fisicamente isolada de implantações que não sejam do governo dos EUA;
          Acessível somenta a pessoal verificado e autorizado;

      #Azure China;
        Microsoft é o primeiro provedor estrangeiro de serviços de nuvem pública da China, em conformidade com as regulamentações governamentais;
        Fisicamente separada dos serviçoes de nuvem do Azure operados pela 21Vianet;
        Todos os dados permanecem dentro da China para garantir a conformidade;

  #Recursos do Azure;
  
      #Grupo de recursos;
        Um amontoado de recursos que você tem para ter uma organização para saber onde locilizar o que precisa;
        Um grupo de recursos é um contêiner que você usa para gerenciar e agregar recursos em uma unica unidade;
        Recursos podem existir em apenas um grupo de recursos;
        Recursos podem existir em diferentes regiões;
        Podem ser movidos para diferentes grupos;
        Aplicativos podem utilizar vários grupos de recursos;
        Posso criar um grupo apenas para VM (Virtual Machine) outro para Banco de dados, etc;
        Ou criar um grupo para um projeto X ou Y;
        Exemplos de recuros;
          Máquinas virtuais;
          Contas de armazenamento;
          Redes virtuais;   
          Serviços de aplicativos;
          Bancos de dados SQL;
          Funções;

  #Assinatura da Azure e Grupos de Gerenciamento;
  
        Uma conta Azure pode ser dividida em várias assinaturas uma para cada setor por exemplo;
          Posso ter uma assinatura do desenvolvimento;
          Assinatura para testes;
          Assinatura de produção;

        Posso ter várias assinaturas na mesma conta Azure desde que esteja pagando;
          Porém só posso ter uma unica conta Azure;

        Separar a conta em varias assinaturas tem uma grande vantagem que consigo saber qual assinatura está                  utilizando quanto para funcionar;

        Uma assinatura do Azure fornece a você acesso autenticado e autorizado às contas do Azure;

        Limite de cobrança;
          Gerar relatórios de cobrança e faturas separados para cada assinatura;

        Limite do controle de acesso;
          Gerenciar e controlar o acesso aos recursos que os usuários podem provisionar com assinaturas específicas;

      #Grupos de gerenciamento;
        Gerenciam e organizam as assinaturas que correspondem a ele;
        Posso gerenciar configurações previas para assinaturas que correpondem a esse grupo;
        As assinaturas herdam as condições aplicadas do grupo de gerenciamento;

#Módulo 2 Cap 2;
  #Tipos de computação;
  #Hospedagem de aplicativos;
  #Redes virtuais;

  #Computação em rede;
  
    Serviços de computação do Azure;
      A computação do Azure é um serviço sob demanda que fornece recursos de computação, como discos, processadores, memória, rede e sistemas operacionais;

  #Máquinas virtuais do Azure;

    As máquinas virtuais do Azure (VMs) são emulações de software de computadores físicos;
    Inclui processador virtual, memória, armazenamento e rede;
    Oferta de IaaS que oferece personalização e controle total;
    Tenho acesso a tudo menos ao hardware físico;


  #Conjuntos de dimensionamento de VMs
  
      Os conjuntos de dimensionamento oferecem uma oportunidade de balanceamento de carga para dimensionar os recursos automaticamente;
    
    Conjuntos de disponibilidade de VMs
      Domínio de falha;
        O rack físico própriamente dito;
      Domínio de atualização;
        Sãos as VMs dentro dos Domínios de falha;
        Idealmente usar varios Domínios de falhas para distribuir suas VMs;

  Área de trabalho virtual do azure;

    Está area é uma virtualização de área de trabalho e aplicativo executada na nuvem;
    Cria um ambiente completo de virtualização da área de trabalho sem precisar executar outros servidores de gateway;
    Reduz risco de que o recurso seja deixado para trás;
    Implantações reais de várias sessões;
    
    Modelo Multisessão;
      Varias pessoas acessam a mesma área de trabalho, porém, cada uma tem sua pasta para trabalho;

    Modelo exclusivo;
      Uma pessoa tem acesso a uma área de trabalho só para ela;

  Serviços de contêineres do Azure;

    Os contêineres do Azure fornecem um ambiente leve e virtualizado que não exige o gerenciamento do sistema operacional e pode responder a alterações sob demanda;
    O contêiner é leve, pode ser recriado ou removido quando quiser;

    Instâncias de Contêiner do Azure;
      Uma oferta de PaaS que executa um contêiner ou pod de contêineres no Azure;

    Aplicativos de Contêiner do Azure;
      Uma oferta de PaaS, como instâncias de contêineres, que pode balancear a carga e escalar;

    Serviço de Kubernetes do Azure (AKS);
      Um serviço de orquestração para contêineres com arquiteturas distribuídas e grandes volumes de contêineres;

  Azure Functions;

    Oferta de PaaS que dá suporte a operações de computação sem servidor;

    O código beseado em EVENTOS é executado quando chamado, sem exigir uma INFRAESTRUTURA DE SERVIDOR durante períodos inativos;

    Função executada sempre que acontece algo, preciso de uma coisa acontecer para iniciar uma Azure Function;

  Comparação de opções de computação do Azure;

    VMs;
      Servidor baseado em nuvem que dá suporte a ambientes Windows ou Linux;
      Útil para migrações de lift-and-shift para nuvem;
        Levar da forma que está;
      Pacote do sistema operacional completo, incluindo o sistema operacional do host;

    Área de trabalho virtual;
      Fornece uma experiência de área de trabalho do Windows baseada em nuvem.
      Aplicativos dedicados para conexão e uso ou acessíveis de qualquer navegador moderno;
      Maior rastreabilidade sobre ações do usuário;

      O logon de vários clientes permite que vários usuários façam logon no mesmo computador ao mesmo tempo;

    Contêineres;
      Ambiente leve e em miniatura adequado para a execução de microsserviços;
      Projeto para escalabilidade e resiliência por meio da orquestração;

      Os aplicativos e serviços são empacotados em contêiner que fica na parte superior do sistema operacional do host. Vários contêineres podem ficar em um sistema operacional do host;

    Serviços de aplicativos do Azure;
      Consistem e muma plataforma totalmente gerenciada para criar, implantar e dimencionar aplicativos Web e APIs rapidamente;
      Trabalha com .NET, .Net Core, Node.js, Java, Python ou PHP;

      Oferta de PaaS como requisitos de nível corporativo de desempenho, segurança e conformidade;

    Serviços de rede do Azure;
      Rede Virtual do Azure (VNet);
        Permite que os recursos do Azure se comuniquem uns com os outros, com a Internet e com as redes locais;

        Pontos de extremidade públicos, acessíveis de qualquer lugar na internet;

        Pontos de extremidade privados, acessíveis somente dentro de sua rede;

        As sub-redes virtuais segmentam sua rede para atenderàs suas necessidades;

        O emparelhamento de rede conecta suas redes privadas diretamente;

        Posso conectar meu ambiente físico ao virtual;
        Vnets não estão linkadas por default, porém, nada me impede de conectar uma a outra, mas isso aumenta o risco de ataques laterais;


      Gateway de VPN;
        O gateway de VPN é usado para enviar tráfego criptografado entre uma rede virtual do Azure e uma no local pela Internet pública;

      ExpressRoute;
        Estende as redes locais para o Azure por meio de conexão privada para facilitar um provedor de conectividade;
        É uma conexão direta de cabo entre o servidor físico e o Datacenter da Microsoft;
        Opção cara, porem, muito segura e bem performatica;

      DNS do Azure;
        Confiabilidade e desempenho aproveitando uma rede global de servidores de nome DNS usando a rede Anycast;
        A segurança do DNS do Azure baseia-se no gerenciador de recursos do Azure, habilitando o controle de acesso;

    
        

        
      
  
    
    

      

      
      




        
        
