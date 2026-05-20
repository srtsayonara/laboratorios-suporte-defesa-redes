# Laboratorio: Configuração de Redes LAN
Este repositório contem o meu projeto prático de redes. Ele foi desenvolvido como parte da minha
formacão em Suporte de Redes e Defesa de Redes para demonstrar conhecimentos praticos de
infraestrutura e organização.
O objetivo foi conectar duas redes de computadores separadas usando um roteador para simular um
ambiente real.

## Como a Rede foi Montada (Topologia)
Dividi o laboratório em duas redes locais (LANs) diferentes ligadas por um roteador para permitir o
controle e a organização da comunicação:
- Rede A: Composta por 2 computadores (PCs) ligados em um Switch. O Switch conecta na interface
do roteador.
- Rede B: Composta por 1 PC e 1 Laptop ligados em outro Switch. Esse Switch tambem conecta na
outra interface do roteador.

## Prints do laboratóriono Packet tracer
()<img width="1366" height="768" alt="imagem1" src="https://github.com/user-attachments/assets/a97d9b39-35c3-4643-a9af-68802e0395d1" />


## Cabos e Camada Física
A rede foi montada utilizando cabos (rede cabeada), o que garante mais estabilidade e melhor
desempenho.
Foi utilizado o Cabo Direto (Straight-Through) para conectar dispositivos de diferentes camadas (PC ->
Switch e Switch -> Roteador).
Com a montagem correta, todas as conexoes ficaram ativas (luzes verdes no Packet Tracer).

## Endereçamento IP
Para organizar os dispositivos, foram utilizadas faixas de IP privadas Classe C:
- Rede A: 192.168.1.X | Mascara: 255.255.255.0
- Rede B: 192.168.2.X | Mascara: 255.255.255.0
A mascara 255.255.255.0 define o tamanho da sub-rede e a quantidade de dispositivos suportados.

## Diagnóstico de Falhas (Troubleshooting)
Inicialmente, os dispositivos da mesma rede se comunicavam corretamente, mas nao havia comunicacao
entre as redes.
O problema foi identificado como falta de configuracao de gateway no roteador.

## Configuração do Roteador

### Rede A
interface gigabitEthernet 0/0
ip address 192.168.1.1 255.255.255.0
no shutdown
exit
### Rede B
interface gigabitEthernet 0/1
ip address 192.168.2.1 255.255.255.0
no shutdown
exit

## Conclusão
Este laboratório demonstra a importância da correta configuracão de redes LAN e do roteamento entre
sub-redes distintas.
O projeto une conceitos de suporte técnico como endereçamento IP e roteamento, mostrando como
esses elementos trabalham juntos em um ambiente real.

## Autoria
### Desenvolvido por
Carla Sayonara Freitas
### Formacao
Estudante de Suporte de Redes e Defesa de Redes

