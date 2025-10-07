# EMS - AlgaSensors Meta

Este repositório é o projeto principal do sistema EMS AlgaSensors, composto por múltiplos microserviços para gerenciamento, monitoramento e processamento de sensores de temperatura.

## Visão Geral

O EMS AlgaSensors é uma solução baseada em microserviços para gerenciar dispositivos de sensores, monitorar leituras de temperatura e processar dados em tempo real. O sistema é dividido em três microserviços principais:

- **Device Management**: Gerencia o cadastro, atualização, remoção e ativação/desativação de sensores.
- **Temperature Monitoring**: Responsável por armazenar e consultar logs de temperatura, além de monitorar o estado dos sensores.
- **Temperature Processing**: Processa dados brutos de temperatura recebidos dos sensores.

## Estrutura do Projeto

```
microservices/
  device-management/
  temperature-monitoring/
  temperature-processing/
```

Cada microserviço possui seu próprio README com instruções específicas.

## Tecnologias Utilizadas

- Java 21
- Spring Boot 3.5.x
- JPA/Hibernate
- H2 Database (para desenvolvimento)
- Lombok
- [hypersistence-tsid](https://github.com/vladmihalcea/hypersistence-tsid) para geração de IDs distribuídos
- Gradle

## Como Executar

Cada microserviço pode ser iniciado individualmente. Exemplo para rodar todos localmente:

1. Acesse a pasta de cada microserviço:
   ```sh
   cd microservices/device-management
   ./gradlew bootRun
   ```
   Repita para os outros microserviços (`temperature-monitoring` e `temperature-processing`).

2. Os serviços estarão disponíveis nas portas:
   - Device Management: `8080`
   - Temperature Monitoring: `8082`
   - Temperature Processing: `8081`

## Submódulos

Este repositório utiliza submódulos Git para cada microserviço. Para clonar com todos os submódulos:

```sh
git clone --recurse-submodules git@github.com:tiquinhonew/ems-algasensors-meta.git
```

## Licença

[MIT License](https://github.com/tiquinhonew/ems-algasensors-meta?tab=MIT-1-ov-file#readme) © Douglas Moraes

---

Para detalhes de cada microserviço, consulte o README respectivo em cada pasta.