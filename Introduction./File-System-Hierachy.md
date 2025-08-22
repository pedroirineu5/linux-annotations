# File System Hierachy

!(Mais sobre FHS!)[https://refspecs.linuxfoundation.org/FHS_3.0/fhs/index.html]

É um padrão que define como os diretórios são organizados em sistemas do tipo Unix/Linux. Com isso facilita a portabilidade de sistemas, administração e compatibilidade entre outras [distros](Linux-Distros).

- **`/` (raiz)**  
    Ponto de partida da árvore de diretórios. Todos os outros diretórios e arquivos estão pendurados nele.
    
- **`/bin`**  
    Contém executáveis essenciais do sistema, usados tanto pelo administrador quanto por usuários comuns.  
    Exemplos: `ls`, `cp`, `mv`, `cat`.
    
- **`/sbin`**  
    Executáveis de administração do sistema, geralmente necessários para inicialização ou manutenção.  
    Exemplos: `fsck`, `iptables`, `reboot`.
    
- **`/boot`**  
    Arquivos necessários para a inicialização do sistema (kernel, initrd, bootloader).
    
- **`/dev`**  
    Arquivos especiais que representam **dispositivos de hardware**.  
    Exemplo: `/dev/sda` (disco), `/dev/null`.
    
- **`/etc`**  
    Arquivos de **configuração** do sistema e dos serviços.  
    Exemplo: `/etc/passwd`, `/etc/fstab`.
    
- **`/home`**  
    Diretório pessoal dos usuários comuns.  
    Exemplo: `/home/pedro`.
    
- **`/lib`**  
    Bibliotecas essenciais compartilhadas pelos programas em `/bin` e `/sbin`.
    
- **`/media`**  
    Ponto de montagem para mídias removíveis (pendrives, CDs, DVDs).
    
- **`/mnt`**  
    Ponto de montagem genérico, usado para montagens temporárias de dispositivos ou partições.
    
- **`/opt`**  
    Local para instalação de softwares opcionais de terceiros (fora do sistema principal).
    
- **`/proc`**  
    Sistema de arquivos virtual com informações sobre o kernel e processos em tempo real.  
    Exemplo: `/proc/cpuinfo`, `/proc/meminfo`.
    
- **`/root`**  
    Diretório pessoal do superusuário (**root**).
    
- **`/run`**  
    Armazena informações de runtime, como PID de processos e sockets de serviços.
    
- **`/srv`**  
    Dados específicos de serviços (como sites de um servidor web).
    
- **`/sys`**  
    Sistema de arquivos virtual que exporta informações sobre os dispositivos e o kernel.
    
- **`/tmp`**  
    Arquivos temporários (podem ser apagados após reboot).
    
- **`/usr`**  
    Contém a maior parte dos programas e dados de uso geral.
    
    - `/usr/bin` → executáveis não essenciais ao boot.
        
    - `/usr/sbin` → utilitários de administração não críticos.
        
    - `/usr/lib` → bibliotecas.
        
    - `/usr/share` → documentação, manuais, ícones etc.
        
- **`/var`**  
    Arquivos variáveis que mudam frequentemente.  
    Exemplo: logs em `/var/log`, spool de impressoras, cache de pacotes.

Vamos por a mão na massa!

Use a sua Máquina local, Vagrant ou Virtual Machine para viajar pelos diretórios.

![[Diretorios-na-pratica.png]]


Na primeira linha podemos ver o comando `ls` que é um comando para listar todos os diretórios da pasta onde você está. Com isso eu só fui retornado a um `.cfg`, pois ainda não estava no diretório raiz da minha VM.

Usei o comando `cd /`  para me locomover para o diretório raiz