# 🖧 Laboratório de Redes - VLANs e Sub-redes

Este repositório contém a documentação, topologia e arquivos de configuração de um laboratório de redes criado para estudo prático com **GNS3 + VMware Workstation**.  
O objetivo é consolidar conhecimentos técnicos em **VLANs, sub-redes e roteamento entre VLANs** em um ambiente realista, reproduzível e usando somente software gratuito.

---

## 🔹 Objetivos do Projeto
- Criar um ambiente de laboratório de redes virtualizado.
- Configurar VLANs para diferentes departamentos de uma empresa fictícia.
- Implementar sub-redes com endereçamento IP planejado.
- Testar comunicação entre hosts em diferentes VLANs.
- Documentar todo o processo para fins de portfólio técnico.

---

## 🛠️ Ferramentas Utilizadas
- **GNS3** → simulação da topologia de rede.
- **VMware Workstation Player** → máquinas virtuais Linux/Windows para simular hosts e servidores.
- **VSCode** → edição de configs e documentação.
- **Sistemas Operacionais**:
  - Windows 10 (host principal)
  - Linux Ubuntu/Debian (servidores DNS/DHCP opcionais)
  - Router/Switch Cisco (imagens no GNS3)

---

## 🏗️ Topologia da Rede

📌 Exemplo de cenário simulado (empresa fictícia):

- **VLAN 10 → Vendas** → `192.168.10.0/24`
- **VLAN 20 → TI** → `192.168.20.0/24`
- **VLAN 30 → Administração** → `192.168.30.0/24`

🔗 O diagrama será criado no **draw.io** ou exportado do **Packet Tracer/GNS3** e ficará disponível em:  
`/docs/topologia.png`

```mermaid
graph TD
    R[Router On a Stick] ---|Trunk| S[Switch Layer 2]
    S --- PC1[VLAN 10 - Vendas]
    S --- PC2[VLAN 20]()
