Primeira coisa que acontece é quando você(usuário) liga o botão **POWER** onde energizamos o sistema, e assim passamos para a fase de **POST**, ele testa o hardware vendo se está tudo correto, será explicado nos próximos capítulos. Assim, passando para a **BIOS** verificar a ordem de boot, verificando os dispositivos, **MBR** e **EFI**. **MBR** é uma tabela de partição do disco, limitado a apenas 4 partições fora ser bastante antigo.  Terminando de carregar a BIOS. Terminando de carregar a bios passa para o BootLoader(**GRUB**), passando a ação para o Kernel que é o coração do sistema, chamando o **Initrd**, ele mantém alguns drivers para descarregar na memoria para inicializar o sistema. **Init**.

Recapitulando, seguindo de cima para baixo:

## Power

- Precionar o botão de ligar
- Alimentando todos os Elementos interno

## POST

- Testa todos os componentes por algum problema de hardware, ele quem faz os *bips* quando se tem algum problema com o maquinário.
- Caso passe em todos os teste passa para a BIOS

## BIOS

- Carrega o firmware que está na CMOS(aquela pilhazinha) da placa-mãe;
- Contém ordem de boot e informações de hardware;
- Pegando o primeiro device/dispositivo para iniciar a leitura.

## MBR

