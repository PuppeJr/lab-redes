

---

# Laboratório de Redes - VLANs, Sub-redes e Serviços

Este laboratório tem como objetivo simular um ambiente de rede corporativo, explorando a configuração de **VLANs**, **sub-redes** e a implementação de serviços essenciais como **Active Directory**, **DNS** e **DHCP**.

---

## 🛠️ Ferramentas

- **VMware Workstation**: Hospeda máquinas virtuais, incluindo o servidor Windows Server (AD, DNS, DHCP).  
- **GNS3**: Emulação de dispositivos de rede (roteadores, switches) e integração com máquinas virtuais.  
- **VSCode**: Editor de código para documentação e scripts.  
- **GitHub**: Repositório para versionamento e compartilhamento dos arquivos do laboratório.  

---

## 🌐 Topologia

A topologia de rede consiste em um **roteador central** e **switches** que interligam diferentes VLANs, cada uma representando um departamento específico da empresa.  
O servidor **Windows Server** fornece serviços de diretório e endereçamento IP para as estações de trabalho.

### 📋 Tabela de Endereçamento IP e VLANs

| VLAN ID | Nome da VLAN   | Rede IP        | Máscara         | Gateway       |
|---------|----------------|----------------|-----------------|---------------|
| 10      | VENDAS         | 192.168.10.0   | 255.255.255.0   | 192.168.10.1  |
| 20      | TI             | 192.168.20.0   | 255.255.255.0   | 192.168.20.1  |
| 30      | ADMIN          | 192.168.30.0   | 255.255.255.0   | 192.168.30.1  |
| 99      | GERENCIAMENTO  | 192.168.99.0   | 255.255.255.0   | 192.168.99.1  |

📂 Para o diagrama completo da topologia, consulte o diretório `/docs`.

---

## ⚙️ Configurações

### 🔹 Switches
- Criação e atribuição de VLANs às portas.  
- Configuração de portas **trunk** para comunicação inter-VLAN.  
- Configuração de portas de **acesso** para estações de trabalho.  

### 🔹 Roteador
- Configuração de **sub-interfaces** para roteamento inter-VLAN.  
- Definição de **gateways** para cada VLAN.  

### 🔹 Servidor (Windows Server)
- **Active Directory (AD):** Instalação e configuração do domínio.  
- **DNS:** Configuração de zonas e registros para resolução de nomes.  
- **DHCP:** Criação de escopos para cada VLAN (endereços IP, gateway e servidores DNS).  

---

## ✅ Testes de Conectividade e Serviços

- **Ping:** Verificação de conectividade entre hosts em diferentes VLANs.  
- **Nslookup:** Teste de resolução de nomes DNS.  
- **Login no Domínio:** Validação do ingresso de estações de trabalho no AD.  

---

## 🔄 Reprodução do Laboratório

1. **Abrir projeto no GNS3**: Carregue o arquivo `.gns3` localizado na raiz do repositório.  
2. **Importar VMs no VMware**: Adicione o servidor e as estações de trabalho.  
3. **Configurar Interfaces**: Ajuste as configurações de rede das interfaces virtuais no VMware conforme as VLANs.  
4. **Validar Comunicação**: Execute ping, nslookup e login no domínio.  

---

## 🚀 Próximos Passos

- Adicionar servidor **Asterisk** para implementar serviços de **VoIP**.  
- Desenvolver **scripts de automação** (ex.: Python, Ansible).  
- Documentar **troubleshooting** para problemas comuns.  

---

## 📂 Estrutura do Repositório

lab-redes/ ├── configs/       # Arquivos de configuração dos dispositivos de rede ├── docs/          # Diagramas de topologia e documentação adicional ├── scripts/       # Scripts de automação (Python, Ansible, etc.) ├── screenshots/   # Capturas de tela dos testes e validações └── README.md

---

## 📜 Licença e Créditos

Este projeto é de caráter **acadêmico**, desenvolvido para fins de estudo e como parte de um **portfólio de engenharia de redes**.  

Sinta-se à vontade para utilizar, modificar e distribuir este material, desde que para fins **não comerciais** e com a devida atribuição.


---

👉 Esse arquivo já está pronto pra você salvar como README.md no VSCode e depois subir no GitHub com:

git add README.md
git commit -m "Adicionando documentação inicial do laboratório"
git push


---

Quer que eu te mostre agora como organizar a pasta do projeto (configs, docs, scripts, screenshots) antes de subir no GitHub?

