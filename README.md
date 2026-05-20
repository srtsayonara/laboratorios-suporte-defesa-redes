# Laboratório: Configuração de Redes LAN

Este contém o meu projeto prático de redes. Ele foi como parte da minha mão em Suporte de Redes e Defesa de Redes parapersonagens de demonstração de competências práticas de organização de e.

O objetivo foi tomicor duas redes de computadores de computadores um para roteador simular um ambiente real.

----

## 🏗️Como a Rede foi Montada (Topologia)

Dividi o laboratório em duas redes locais (LANs) diferentes de um roteador para permitir o controle e a organização comunicação da comunicação:

- **Rede A:** Composta por 2 computadores (PCs) nisions em um Switch. O Switch connecta na interface do roteador.
- **Rede B:** Composta por 1 PC e 1 Laptop nisioso em outro Switch. Esse Switch uso coneine na outra interface do roteador do.

----

## 🔌Cabos e Camada Física

A rede foi montada cabos (rede cabeada), o que mais estabilidade e desempenho de desempenho.

Foi utilizado o **Cabo Direto (Straight-Through)** para dispositivos para dispositivos de camadas diferentes (PC → Switch e Switch → Roteador).

Com um ponto alto, demount, todas como conexões como fica umas vivas (luzes verdes no Packet Tracer).

----

## Prints do Projeto Visual

*(Clique nas abass para ver como abaixo do projeto imagens)*

----

## 📐Endereçamento IP

Para organ os dispositivos, foram faixas de faixas de privadas IP Classe C:

- **Verificar A:** 192.168.1. X | Máscara: 255.255.255.0
- **Vermelho B:** 192.168.2. X | Máscara: 255.255.255.0

A máscara 255.255.255.0 define o da quantidade sub-rede e a quantidade de dispositivos suportados.

----

## 🛠️Diagnóstico de Falhas (Solução de Problemas)

Os dispositivos da rede se comunicavam, mas não mas não entre como redes de comunicação.

O problema foi como identificado falta de configuração de gateway no roteador.

----

## 🛠️Configuração do Roteador

### 🌐networking A

interface gigabitEthernet 0/0
ip adsress 192.168.1.1 255.255.255.0
no shutdown
saída

### 🌐 Networking B

interface gigabitEthernet 0/1
ip address 192.168.2.1 255.255.255.0
No shutdown
exit

----

## 🚀 Conclusão

Este laboratório demonstra a importância da correta de redes de redes LAN e do roteamento entre sub-redes

O projeto une conceitos de suporte comozedere técnico IP e roteamento, mostrando como como juntos elements em um trabalho ambiente real.

----

## 👩 💻 Autoria

### 📝 Desenvolvido por

Carla Sayonara Freitas

### 🎓 Formação

Estudante de Suporte de Redes e Defesa de Redes
