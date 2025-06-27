# Criando Máquinas Virtuais no Microsoft Azure

Criar uma Máquina Virtual (VM) no Microsoft Azure é um processo direto que pode ser realizado através do portal do Azure, da CLI do Azure (Command-Line Interface) ou do Azure PowerShell. Este documento focará na criação via portal, que é a abordagem mais visual e intuitiva para iniciantes.

## Pré-requisitos

Antes de começar, certifique-se de ter:

*   Uma conta ativa do Azure. Se não tiver, você pode criar uma conta gratuita com créditos iniciais. [1]
*   Conhecimento básico sobre os conceitos de rede e computação em nuvem.

## Passos para Criar uma VM via Portal do Azure

Siga os passos abaixo para provisionar sua primeira VM no Azure:

### 1. Acessar o Portal do Azure

Abra seu navegador e navegue até o [Portal do Azure](https://portal.azure.com/ ). Faça login com suas credenciais da conta Microsoft.

### 2. Iniciar a Criação da VM

No painel do Portal do Azure, você pode:

*   Clicar em **"Criar um recurso"** no menu lateral esquerdo e pesquisar por "Máquina virtual".
*   Ou, na barra de pesquisa superior, digitar "Máquinas virtuais" e selecionar a opção correspondente.

Na página de Máquinas Virtuais, clique em **"Criar"** e, em seguida, selecione **"Máquina virtual do Azure"**.

### 3. Configurações Básicas (Guia "Noções básicas")

Esta guia é onde você define as configurações essenciais da sua VM:

*   **Assinatura:** Selecione a assinatura do Azure que será usada para faturamento.
*   **Grupo de recursos:** Crie um novo grupo de recursos ou selecione um existente. Grupos de recursos são contêineres lógicos para seus recursos do Azure.
*   **Nome da máquina virtual:** Insira um nome exclusivo para sua VM (ex: `minha-primeira-vm`).
*   **Região:** Escolha a região do Azure onde sua VM será implantada. Selecione uma região geograficamente próxima para menor latência.
*   **Opções de disponibilidade:** Para ambientes de produção, considere configurar conjuntos de disponibilidade ou zonas de disponibilidade para garantir alta disponibilidade.
*   **Tipo de segurança:** Escolha entre Padrão ou Inicialização Confiável (Trusted Launch) para segurança aprimorada.
*   **Imagem:** Selecione a imagem do sistema operacional (SO) para sua VM (ex: Windows Server, Ubuntu Server, Red Hat Enterprise Linux).
*   **Tamanho:** Escolha o tamanho da VM, que define o número de vCPUs, memória e outros recursos. O Azure sugere tamanhos com base na imagem selecionada e na região.
*   **Nome de usuário:** Defina um nome de usuário para a conta de administrador da VM.
*   **Senha:** Crie uma senha forte para a conta de administrador. Esta senha será usada para acessar a VM via RDP (Windows) ou SSH (Linux).
*   **Portas de entrada públicas:** Para fins de teste, você pode permitir portas como RDP (3389) ou SSH (22). Para produção, é recomendável usar um grupo de segurança de rede (NSG) para controlar o acesso.

Após preencher todas as informações, clique em **"Avançar: Discos >"**.

### 4. Configurações de Discos (Guia "Discos")

Nesta guia, você configura o tipo e o tamanho dos discos da sua VM:

*   **Tipo de disco do SO:** Escolha entre SSD Premium, SSD Standard ou HDD Standard. SSD Premium oferece o melhor desempenho.
*   **Criptografia:** Defina as opções de criptografia para o disco do SO.
*   **Discos de dados:** Adicione discos de dados adicionais, se necessário, para armazenar dados de aplicações ou arquivos.

Clique em **"Avançar: Rede >"**.

### 5. Configurações de Rede (Guia "Rede")

Configure a rede virtual e as interfaces de rede para sua VM:

*   **Rede virtual:** Crie uma nova rede virtual ou selecione uma existente. Uma rede virtual é uma rede isolada na nuvem do Azure.
*   **Sub-rede:** Selecione a sub-rede dentro da rede virtual onde a VM será implantada.
*   **IP público:** Crie um novo IP público ou selecione um existente. O IP público permite que sua VM seja acessível pela internet.
*   **Grupo de segurança de rede (NSG):** Configure um NSG para controlar o tráfego de entrada e saída da sua VM. Isso é crucial para a segurança.

Clique em **"Avançar: Gerenciamento >"**.

### 6. Configurações de Gerenciamento (Guia "Gerenciamento")

Esta guia oferece opções para monitoramento, backup e automação:

*   **Diagnóstico de inicialização:** Habilite para solucionar problemas de inicialização da VM.
*   **Identidade:** Configure identidades gerenciadas para permitir que a VM acesse outros recursos do Azure de forma segura.
*   **Desligamento automático:** Programe o desligamento automático da VM para economizar custos.
*   **Backup:** Configure backups para proteger seus dados.

Clique em **"Avançar: Monitoramento >"**.

### 7. Configurações de Monitoramento (Guia "Monitoramento")

Configure as opções de monitoramento para sua VM:

*   **Métricas:** Habilite as métricas básicas para monitorar o desempenho da VM.
*   **Alertas:** Configure alertas para ser notificado sobre eventos importantes ou problemas de desempenho.

Clique em **"Avançar: Avançado >"**.

### 8. Configurações Avançadas (Guia "Avançado")

Esta guia permite configurações mais específicas, como extensões, dados personalizados e tags.

Clique em **"Avançar: Tags >"**.

### 9. Tags (Guia "Tags")

Adicione tags para categorizar e organizar seus recursos do Azure. Isso é útil para gerenciamento de custos e organização.

Clique em **"Avançar: Examinar + criar >"**.

### 10. Revisar e Criar

Revise todas as configurações da sua VM. O Azure realizará uma validação final. Se tudo estiver correto, clique em **"Criar"** para iniciar o processo de implantação da sua VM.

O processo de implantação pode levar alguns minutos. Você pode acompanhar o status no painel de notificações do Azure. Uma vez concluído, sua VM estará pronta para uso.

## Próximos Passos

Após a criação da VM, você pode:

*   Conectar-se à VM via RDP (Windows) ou SSH (Linux).
*   Instalar softwares e aplicações necessárias.
*   Configurar regras de firewall e segurança adicionais.
*   Monitorar o desempenho e a utilização dos recursos da VM.

Este guia fornece uma base sólida para a criação de VMs no Azure. Para cenários mais avançados, explore a documentação oficial do Microsoft Learn. [2]

## Referências

[1] Microsoft Azure. Crie sua conta gratuita do Azure hoje. Disponível em: [https://azure.microsoft.com/pt-br/free/](https://azure.microsoft.com/pt-br/free/ )
[2] Microsoft Learn. Início Rápido: Criar uma VM Windows no portal do Azure. Disponível em: [https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/quick-create-portal](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/quick-create-portal )
