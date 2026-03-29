# 📞 Cisco VoIP Lab – CME + Dial Peer

## 📌 Descrição

Este laboratório simula uma comunicação VoIP entre duas redes distintas utilizando roteadores Cisco com **CME (Call Manager Express)**.

Cada site possui:

* DHCP configurado
* Telefones IP registrados
* Switch multilayer com VLAN de voz
* Roteamento entre redes
* Comunicação via **dial-peer**

---

## 🌐 Topologia

![Topologia](topology/topologia.png)

---

## 🧱 Estrutura da Rede

| Local    | Rede      | Dispositivo       | Ramal |
| -------- | --------- | ----------------- | ----- |
| RH       | 1.1.1.0/8 | IP Phone RH       | 1234  |
| Link WAN | 2.1.1.0/8 | RouterA ↔ RouterB | —     |
| Recepção | 3.1.1.0/8 | IP Phone Recepção | 7890  |

---

## ⚙️ Tecnologias Utilizadas

* Cisco CME (Call Manager Express)
* DHCP Server
* Dial-peer (VoIP)
* VLAN de voz
* Switch multilayer (Layer 3)
* Roteamento IP

---

## 📡 Funcionalidades

* Telefones obtêm IP via DHCP
* Registro automático no CME
* Chamadas entre sites diferentes
* Comunicação via IP (VoIP)
* Segmentação com VLAN de voz

---

## 📂 Configurações

### 🔹 Roteadores

* `routers/RouterA.cfg`
* `routers/RouterB.cfg`

### 🔹 Switches

* `switches/Switch-RH.cfg`
* `switches/Switch-Recepcao.cfg`

---

## 🧠 Conceitos Demonstrados

* Implementação de VoIP em ambiente Cisco
* Configuração de Call Manager Express
* Criação de dial-peers para roteamento de chamadas
* Integração entre múltiplas redes
* Separação de tráfego voz e dados / mas neste caso, só estou usando apenas tráfego de voz!

---

## 🚀 Como testar

1. Ligar os dispositivos no Packet Tracer ou GNS3
2. Garantir que os telefones recebam IP
3. Verificar registro no CME:

   ```
   show ephone registered
   ```
4. Realizar chamadas:

   * RH (1234) → Recepção (7890)
   * Recepção (7890) → RH (1234)

---

## 📌 Autor

Higor Zimmerman
