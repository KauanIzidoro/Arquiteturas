    # Arquitetura baseada em Microsserviços

## Definição

A arquitetura de microsserviços é uma abordagem de desenvolvimento de software na qual o aplicativo é construído como um conjunto de pequenos serviços independentes. Cada serviço é responsável por uma função específica e pode ser desenvolvido, implantado e mantido de forma independente dos outros. Essa arquitetura facilita a implementação de mudanças, a escalabilidade e o desenvolvimento contínuo, fornecendo um framework modular.

## Motivação

- Introduzida por grandes empresas de tecnologia em **2009** para superar limitações da arquitetura monolítica.
- Alinhada à abordagem **Cloud-native**, o que a torna ideal para ambientes em nuvem, onde a escalabilidade e a flexibilidade são essenciais.

## Características

- **Divisão de Aplicativos**: Aplicativos são divididos em múltiplos serviços independentes, cada um com seu próprio ciclo de vida.
- **Escalabilidade e Atualizações Separadas**: Cada serviço pode ser escalado e atualizado de forma independente, sem afetar outros componentes do sistema.
- **Flexibilidade e Resiliência**: Oferece mais flexibilidade na escolha de tecnologias e maior resiliência, já que falhas em um serviço não impactam diretamente outros.

## Vantagens

- **Agilidade**: Equipes podem trabalhar de forma independente em diferentes serviços, acelerando o desenvolvimento.
- **Escalabilidade**: Serviços podem ser escalados individualmente, o que otimiza o uso de recursos.
- **Liberdade Tecnológica**: Cada serviço pode ser desenvolvido utilizando a tecnologia mais adequada ao seu propósito.
- **Código Reutilizável**: A modularidade facilita a reutilização de código e a adoção de boas práticas.

## Desvantagens

- **Complexidade**: A comunicação e a orquestração entre serviços aumentam a complexidade do sistema.
- **Custos**: Manter e operar vários serviços pode gerar custos adicionais, especialmente em ambientes de nuvem.
- **Comunicação**: A troca de informações entre serviços, muitas vezes via APIs, pode introduzir latência e sobrecarga.
- **Segurança**: A maior superfície de ataque requer estratégias mais robustas para garantir a segurança entre os serviços.

## Logs VS Traces:

### Logs:

Apenas registros de eventos que ocorreram.

### Traces:

São mais detalhados, acompanham o fluxo de execução de alguma operação.
