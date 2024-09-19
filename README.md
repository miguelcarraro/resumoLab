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

      




        
        
