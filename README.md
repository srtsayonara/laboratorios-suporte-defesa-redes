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
Inicialmente, os dispositivos da mesma rede se comunicavam corretamente, mas não havia comunicação
entre as redes.
O problema foi identificado como falta de configuração de gateway no roteador.

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
## 🔌 Testando a rede com a "Cartinha" (Ping)

Depois de colocar os dois computadores na mesma rede, usei a ferramenta de simulação do Packet Tracer (o ícone da cartinha) para testar se eles conseguem conversar entre si.

### Como funciona o caminho:
1. **O começo:** A cartinha sai do primeiro computador (**PC0**).
2. **O meio do caminho:** Ela passa pelo **Switch**, que entende para onde ela deve ir.
3. **A entrega:** O Switch entrega a cartinha direto no segundo computador (**PC1**).

### Veja como ficou no mapa:

![Enviando para o Switch](<img width="1366" height="768" alt="interacao_swish" src="https://github.com/user-attachments/assets/af5e08a8-c14b-427c-a6ce-7e3a7c959d93" />
)

![Chegando no destino](<img width="1366" height="768" alt="mensagem_entregue-pc01" src="https://github.com/user-attachments/assets/4c844264-2917-4718-8dea-8fa2a7284aea" />
)

> 👍 **Sucesso!** No final do teste, o Packet Tracer mostra o status como **Successful**, o que significa que os computadores estão conversando perfeitamente.

## 🏁 Conclusão

Este laboratório foi excelente para praticar e demonstrar a montagem de uma topologia de rede do zero no Packet Tracer. 

Comecei criando a estrutura física básica e, logo em seguida, usei o teste das "cartinhas" para validar a comunicação em tempo real. O projeto mostra, na prática, como o endereçamento IP e a configuração correta do roteador fazem toda a diferença para que redes diferentes consigam se conversar.

---
🧑‍💻 **Autor:** Carla Sayonara Freitas
### Formação:
Estudante de Suporte de Redes e Defesa de Redes cursos desenvolvidos pela Cisco Networking Academy
(OBS: esse projeto ainda não foi finalizado, é apenas um registro do que foi aprendido) 
