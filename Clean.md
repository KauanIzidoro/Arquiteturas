# Clean Architecture

## Visão Geral

A **Clean Architecture** é um modelo arquitetural proposto por Robert C. Martin (Uncle Bob) que visa separar as responsabilidades do sistema em camadas, garantindo independência e isolamento entre elas. O foco é criar sistemas fáceis de testar, manter e modificar, além de promover a independência de frameworks e tecnologias externas. A Clean Architecture facilita a construção de sistemas flexíveis e escaláveis, pois prioriza a separação entre as regras de negócio e os detalhes de implementação.

## Principais Componentes

1. **Enterprise Business Rules (Regras de Negócio da Empresa):**  
   Concentram as regras de negócios centrais e fundamentais que governam a operação da organização. Essas regras devem estar completamente isoladas de qualquer dependência externa, garantindo que sejam reusáveis e independentes de frameworks ou interfaces.

2. **Application Business Rules (Regras de Negócio da Aplicação):**  
   Representam os casos de uso e descrevem as operações que a aplicação pode realizar, interagindo com as regras de negócio. Elas são responsáveis pelo fluxo das ações e coordenação dos dados entre as diferentes camadas, mas também não dependem de frameworks ou drivers externos.

3. **Interface Adapters (Adaptadores de Interface):**  
   Fazem a ponte entre as regras de negócio (domínio) e as implementações concretas, como bancos de dados, APIs externas e a interface do usuário. Transformam os dados para um formato que as camadas internas podem usar e vice-versa.

4. **Frameworks e Drivers:**  
   São os detalhes externos do sistema, como frameworks web, bibliotecas de banco de dados, interfaces gráficas e dispositivos de hardware. Esta camada depende de implementações específicas, mas deve ser completamente desacoplada das regras de negócio e casos de uso.

## Vantagens

- **Independência de frameworks:** a lógica de negócio não está acoplada a nenhum framework específico, permitindo troca ou atualização de frameworks com menos impacto.
- **Facilidade de testes:** com a separação de responsabilidades, é mais fácil testar a aplicação isoladamente, testando cada camada de forma independente.
- **Capacidade de manutenção:** o código organizado em camadas claras torna a manutenção e evolução do sistema mais simples e controlada.
- **Flexibilidade:** permite trocar implementações de infraestrutura sem alterar as regras de negócio.
- **Escalabilidade:** por ser modular, a Clean Architecture facilita a adição de novas funcionalidades sem grandes mudanças estruturais.
- **Reusabilidade:** as regras de negócio podem ser reutilizadas em diferentes contextos e interfaces.

## Desvantagens

- **Complexidade de implementação:** a arquitetura pode ser mais difícil de implementar, especialmente em projetos menores.
- **Curva de aprendizado:** exige que os desenvolvedores compreendam profundamente os princípios de design arquitetural, o que pode aumentar a curva de aprendizado.
- **Sobrecarga para projetos simples:** em projetos pequenos, a divisão de camadas pode parecer excessiva e desnecessária.
- **Maior tempo de desenvolvimento:** a separação rigorosa das camadas e a modularidade podem aumentar o tempo inicial de desenvolvimento.
- **Gerenciamento de dependências:** a necessidade de manter cada camada desacoplada pode resultar em uma maior complexidade no gerenciamento de dependências.

## Fitness Functions

As **Fitness Functions** são técnicas automatizadas que verificam continuamente a saúde e a integridade arquitetural de um sistema. No contexto da Clean Architecture, elas podem incluir métricas para monitorar:

- **Independência de Camadas:** garantir que camadas mais internas não dependam de camadas externas.
- **Cobertura de Testes:** manter uma alta cobertura de testes unitários e de integração para cada camada do sistema.
- **Complexidade Ciclomática:** monitorar a complexidade do código para assegurar que a simplicidade seja mantida nas camadas internas.

## Cobertura de Teste por Camada

É essencial garantir que cada camada da Clean Architecture seja bem testada:

- **Enterprise Business Rules:** devem ter testes unitários extensivos para garantir que as regras de negócio fundamentais funcionem corretamente.
- **Application Business Rules:** testes de integração que validem os casos de uso e como as regras de negócio interagem.
- **Interface Adapters:** testes de integração para verificar se a comunicação entre as camadas internas e as externas está funcionando adequadamente.
- **Frameworks e Drivers:** devem ser cobertos por testes de integração ou mocks, garantindo que os detalhes de implementação não impactem as outras camadas.


### Princípio da Inversão de Dependência (DIP)

Um dos princípios centrais da Clean Architecture é o **Princípio da Inversão de Dependência (Dependency Inversion Principle - DIP)**. Este princípio garante que as camadas mais internas (domínio e casos de uso) nunca dependam das camadas externas (como frameworks e interfaces). Em vez disso, as dependências fluem das camadas externas para as internas, utilizando abstrações como interfaces para injeção de dependência.

### Separation of Concerns

A **Clean Architecture** enfatiza a **separação de responsabilidades** (Separation of Concerns), que permite que diferentes aspectos do sistema sejam desenvolvidos e mantidos de forma independente, sem misturar preocupações como lógica de negócios, persistência de dados e interface do usuário.

### Camadas e Círculos Concêntricos

A Clean Architecture é frequentemente representada como círculos concêntricos, onde cada camada mais interna não conhece as camadas externas. As regras de negócios da empresa estão no centro, enquanto as interfaces, frameworks e drivers estão nas camadas mais externas. As dependências fluem sempre de fora para dentro, nunca o contrário.

---

