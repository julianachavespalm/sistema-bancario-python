# Sistema Bancário em Python

## 1. Objetivo
Este sistema bancário foi desenvolvido como parte de um desafio da Digital Innovation One (DIO), proposto pelo professor Guilherme Carvalho. O objetivo é simular as principais operações: **Depósito**, **Saque** e **Visualização de Extrato**. O sistema foi projetado para um único usuário, sem a necessidade de validação de contas ou gerenciamento de múltiplos usuários. Todas as regras de negócio se aplicam exclusivamente a esse usuário.

## 2. Funções
O sistema implementa as seguintes funções:

1. **Depósito**: O usuário pode depositar valores maiores que zero. O valor depositado será somado ao saldo e registrado no extrato.
2. **Saque**: O usuário pode realizar saques com limite de até R$ 500,00 por operação e um máximo de 3 saques por dia. O valor será descontado do saldo e registrado no extrato.
3. **Visualização de Extrato**: Exibe todas as operações de depósito e saque, bem como o saldo atual da conta, atualizados em tempo real.

## 3. Como Rodar o Sistema no Google Colab

### 3.1 Acessar o Sistema

O sistema bancário está hospedado no Google Colab. Para rodá-lo, siga os passos abaixo:

1. Clique no link a seguir para acessar o notebook no Google Colab: **[Sistema Bancário - Google Colab](link_do_notebook)**.
2. No Google Colab, clique no botão **"Conectar"** no canto superior direito para inicializar o ambiente.
3. Após a conexão, clique no botão **"Executar Tudo"** para rodar o sistema interativo.

### 3.2 Interação

O sistema apresentará um menu interativo no terminal do Google Colab, onde você poderá escolher entre as seguintes opções:
- **[d] Depositar**
- **[s] Sacar**
- **[e] Extrato**
- **[q] Sair**

Basta inserir a opção desejada e seguir as instruções fornecidas.

## 4. Funcionalidades do Sistema

### 4.1 Depósito

#### Valores aceitos
- Somente valores maiores que zero são permitidos para depósito.

#### Registro no saldo
- O valor depositado é somado ao saldo da conta do usuário.

#### Registro no extrato:
- O sistema registra a quantidade de depósitos realizados.
- O valor depositado é armazenado no formato R$ XXX.XXX,XX.
- O registro inclui a data da operação no formato `dd/mm/YYYY` e a hora no formato `HH:MM`.

#### Depósitos inválidos
- Depósitos de valores iguais ou menores que zero são rejeitados.
- Uma mensagem de erro será exibida, e a operação não será registrada no saldo nem no extrato.

### 4.2 Saque

#### Limite por saque
- O valor máximo permitido por saque é de R$ 500,00.

#### Limite diário
- O usuário pode realizar até 3 saques por dia. Após atingir o limite, novos saques são bloqueados até o próximo dia.

#### Saldo disponível
- O usuário só pode sacar valores até o saldo disponível. Saques superiores ao saldo são rejeitados com uma mensagem de erro.

#### Registro no saldo
- O valor do saque é subtraído do saldo da conta.

#### Registro no extrato
- Cada saque realizado com sucesso é registrado no extrato, no formato R$ XXX.XXX,XX, e inclui a data e hora da operação.

#### Saques inválidos
- Tentativas de saque com valor superior a R$ 500,00, saldo insuficiente ou após 3 saques no mesmo dia são rejeitadas. O sistema exibe mensagens de erro apropriadas, e a operação não afeta o saldo nem o extrato.

### 4.3 Visualização de Extrato

#### Histórico de operações
- O usuário pode visualizar todas as operações de depósito e saque realizadas na conta.

#### Exibição do saldo
- O saldo atual da conta é exibido no final do extrato.

#### Formato de valores
- Todos os valores são exibidos no formato monetário: R$ XXX.XXX,XX.

#### Registro de data e hora
- Cada transação no extrato inclui a data (`dd/mm/YYYY`) e a hora (`HH:MM`).

#### Atualização em tempo real
- O extrato é atualizado em tempo real após cada operação de depósito ou saque.
