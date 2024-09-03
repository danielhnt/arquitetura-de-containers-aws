## Arquitetura de Containers na AWS

A AWS oferece um conjunto robusto de serviços para construir, implantar e gerenciar aplicações baseadas em containers, permitindo maior agilidade, escalabilidade e controle sobre suas aplicações.

### 1. Amazon Elastic Container Service (ECS)
- **Gerenciamento Simples:** ECS é um serviço gerenciado que facilita a execução de containers Docker. Com ele, você pode orquestrar e gerenciar clusters de containers sem precisar gerenciar a infraestrutura subjacente.
- **Modos de Execução:** ECS oferece dois modos principais: EC2, onde você gerencia as instâncias subjacentes, e Fargate, um serviço sem servidor que lida com a infraestrutura para você.

### 2. Amazon Elastic Kubernetes Service (EKS)
- **Orquestração com Kubernetes:** EKS é um serviço gerenciado que permite executar Kubernetes na AWS, fornecendo toda a robustez do Kubernetes com a flexibilidade e segurança da AWS. Ele facilita o escalonamento de aplicações containerizadas e oferece integração profunda com outros serviços da AWS.
- **Autogerenciamento:** Embora EKS gerencie o plano de controle Kubernetes, você pode personalizar e otimizar seus nós de trabalho (workloads) conforme necessário.

### 3. Amazon Elastic Container Registry (ECR)
- **Armazenamento de Imagens Docker:** ECR é um repositório de imagens Docker altamente disponível, seguro e escalável. Ele se integra diretamente com ECS e EKS, facilitando o ciclo de vida de imagens de container na AWS.

### 4. AWS Fargate
- **Execução Sem Servidor:** Fargate permite executar containers sem precisar provisionar ou gerenciar servidores, liberando a equipe de operações para focar em tarefas de maior valor agregado.
- **Escalonamento Dinâmico:** Com Fargate, o escalonamento é dinâmico e baseado na necessidade do workload, otimizando o uso de recursos e custos.

### 5. Infraestrutura como Código (IaC)
- **Automação com Terraform:** Usar Terraform para gerenciar a infraestrutura de containers na AWS proporciona controle versionado e reprodutível de clusters, redes e outras configurações.
- **AWS CloudFormation:** Outra opção é usar o CloudFormation, o serviço nativo da AWS para gerenciamento de infraestrutura como código, simplificando a implantação e o gerenciamento de stacks de containers.

### 6. Rede e Segurança
- **VPC e Segurança:** A arquitetura de containers na AWS permite isolar workloads dentro de VPCs, controlar o tráfego com security groups, e aplicar políticas de rede refinadas com Network ACLs e políticas de segurança do Kubernetes.
- **Integração com IAM:** Controle o acesso aos recursos de container usando IAM roles, policies e service accounts, garantindo que cada componente tenha as permissões adequadas.

### 7. Monitoramento e Logging
- **Amazon CloudWatch:** Integrar CloudWatch com ECS e EKS permite monitorar métricas, logs e criar alarmes para eventos críticos, facilitando a observabilidade dos seus serviços.
- **AWS X-Ray:** Para rastreamento de performance e debugging, o X-Ray fornece insights sobre a interação de diferentes componentes de sua aplicação containerizada.

### 8. Melhores Práticas
- **Imutabilidade:** Implemente práticas de imutabilidade, onde containers são tratados como efêmeros e imagens são versionadas e imutáveis.
- **Escalabilidade Horizontal:** Prefira escalar horizontalmente (adicionar mais containers) ao invés de verticalmente (aumentar o poder de um container individual).
- **Segurança:** Sempre mantenha suas imagens atualizadas e use scanners de vulnerabilidade para garantir que seus containers estejam livres de falhas de segurança conhecidas.

## Abaixo seguem relacao das

### [Day 1 - Arquitetura de VPC's](/Arquitetura_de_Containers/day1/README.md)

### [Day 2 - ECS: Elastic Container Service](/Arquitetura_de_Containers/day2/README.md)