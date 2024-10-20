# Desafio Terraform - Estágio

## 1. Descrição Técnica do Projeto

Este projeto se trata de um desafio de estágio e tem como objetivo descrever uma infraestrutura na AWS usando o Terraform. A infraestrutura consiste em:

### 1.1. Recursos Criados
- **Provider AWS**: Define o provedor AWS na região `us-east-1`.
- **Variáveis**:
  - `projeto`: Nome do projeto (padrão: "VExpenses").
  - `candidato`: Nome do candidato (padrão: "SeuNome").
  
- **TLS Private Key**: Gera uma chave privada para acessar a instância EC2.
- **AWS Key Pair**: Cria um par de chaves para permitir o login SSH na instância.
- **VPC (Virtual Private Cloud)**: Cria uma rede virtual para o projeto, onde os recursos serão provisionados.
- **Subnet**: Cria uma subnet dentro da VPC, associada à zona de disponibilidade `us-east-1a`.
- **Internet Gateway**: Cria um gateway para permitir o acesso à internet.
- **Route Table e Association**: Configura rotas de internet para a VPC.
- **Security Group**: Define regras de firewall para permitir tráfego SSH (porta 22) e todo o tráfego de saída.
- **AWS EC2 Instance**: Provisionei uma instância EC2 baseada no Debian 12 com 20 GB de armazenamento.
- **Outputs**:
  - `private_key`: Exibe a chave privada para acessar a instância EC2.
  - `ec2_public_ip`: Exibe o endereço IP público da instância EC2.
