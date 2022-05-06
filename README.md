# Acer-Nitro-AN517-51-55-OpenCore-EFI (OpenCore 0.81) - Atualizado OpenCore, DSDT e KEXTS
Essa EFI não faz uso de SSDT, todos os patchs ACPI foram feitos no SDST.
#Hackintosh, MacOS Monterey, MacOS
<h2>EFI OpenCore para o notebook Acer Nitro 5 AN517-51-55 (17 Polegadas, Core i5 9300H, Geforce 1650, Intel UHD 630)</h2>

Detalhamento do que funciona e não funciona<br />

<details><summary>Português do Brasil</summary>
<h2>O que não funciona?</h2>
Hardware: Geforce 1650M - NVidia Optimus {<br />
HDMI (Geforce Optimus, não funciona de jeito nenhum)}<br />
Hardware Proprietário:<br />
Apple AirDrop<br />

<h2>O que funciona?</h2>
<h2>TOUCHPAD (Com todas as gestures, perfeito)</h2>
iGPU (Intel UHD 630)<br />
Controlador nVme<br />
Controlador Sata<br />
Áudio<br />
Controladores de Rede (ETH e WiFi)<br />
Portas USB (Inclusive a 3.1)<br />
Porta USB-C (4gbps)<br />
Sensor de Bateria<br />
Sensores da CPU (Temperatura)<br />
Entrada de Fone de Ouvido e Microfone<br />
Microfone embutido<br />
Webcam Embutida<br /><br />

<h2>Atalhos do Teclado - via Tecla de Função (FN))</h2>
<h3>Funciona:</h3>
[FN]+[F4] - Modo de Suspensão<br />
[FN]+[F6] - Desliga o LCD<br />
[FN]+[F8] - Desabilita o Áudio (mudo)<br />
[FN]+[F7] - Habilita/Desabilita o Touchpad (FUNCIONANDO!!!)<br />
[FN]+[F9] - Diminui a retroiluminação do teclado<br />
[FN]+[F10] - Aumenta a retroiluminação do teclado<br />
[FN]+[F11] - Aumenta o Brilho da tela<br />
[FN]+[F12] - Diminui o Brilho da tela<br />
[FN]+[Pg Up] - Inicia o App do Apple Music<br />
[FN]+[Seta pra Esquerda/Direita] Diminui/Aumenta o Brilho da Tela<br />
[FN]+[Seta para Baixo/Cima] Diminui/Aumenta o Volume<br />
<h3>Não Funciona:</h3>
[F3] - Alternar WiFi ligado e desligado<br />
[F5] - Alternar Display (Vídeo Interno / Externo (HDMI))</details>

<details><summary><em>Instruções para CRIAR o Pendrive do MacOS Monterey (ou a versão de sua preferência) com a EFI e o BaseSystem.dmg</em></summary>
<h4>Este método foi tentado apenas com o modo de restauração, então faça o boot pelo Pendrive com a ferramaenta disponibilizada no pacote</h4><br />
Para usar este método é mandatório que você siga os passos abaixo:<br /><br />
Use o script mountEFI para montar a partição EFI do seu pendrive, caso você já tenha um funcional, com outro sistema operacional para instalação, caso contrário, apenas formate o Pendrive em FAT32, e copie a pasta EFI para a raiz do Pendrive.<br /><br />
Note que nesse caso específico você não precisa de um Pendrive de 16Gb, pois não vamos usar a imagem completa do sistema, um de 1 ou 2gb já será o suficiente.<br /><br />
Instale a última versão do Python no seu sistema operacional (mandatório se você for fazer isso pelo MacOS)<br />
Um script Python de nome macrecovery.py, está dentro da pasta Utils/macrecovery<br /><br />
Execute o programa e escolha a opção que você deseja</em><br /><br />
Após o download, vá até o pendrive onde está a EFI e crie uma pasta chamada <b><em>com.apple.recovery.boot</b></em> a pasta precisa ter EXATAMENTE este nome, ou o processso não vai funcionar.<br />
  coloque o arquivo baixado dentro da pasta criada.<br /><br />
Foi usado o pacote do MacOS Monterey, com a última versão baixada diretamente dos repositórios da Apple, <b>12.1</b> (BaseSystem.dmg - usado apenas para dar o boot inicial, toda instalação é feita pela internet)<br /><br />
Desative na sua bios as opções de virtualização da Intel e AMD, todas que forem possíveis<br />
MUDE os contrtoladores de disco para AHCI, não deixe em SATA, IDE, ou qualquer outro pois o sistema não suporta nenhum outro padrão, apenas AHCI... após a instalação você pode ver se existe algum modo para usar com outra opção fora AHCI, no caso de você ter uma placa que suporte a Tecnologia da Intel "RST OPTANE" ou "RST PREMIUM OPTANE" mas não deixe habilitado na instalação ou o sistema vai travar (KERNEL PANIC)<br /><br />
DESATIVE o SecureBoot durante a instalação, novamente você poderá ver se existe alguma possibilidade de ativar novamente depois da instalação, se você já tem uma instalação do Windows, que não está em AHCI, sugiro que mude para AHCI, e instale o Windows novamente, ou procure na internet como reparar uma instalação do Windows 10 ou 11 após mudar os controladores de disco para AHCI<br /><br />
Eu não vou entrar em detalhes de como utilizar a tecnologia "OPTANE" da intel nesse guia, nem de como ativar o SecureBoot e opções de Virtualização, após executar a instalação, porque foge do escopo pretendido.</details>

<h2>EFI OpenCore for notebook Acer Nitro 5 AN517-51-55 (17 Inch., Core i5 9300h, Geforce 1650, Intel UHD 630)</h2>

Details about what Work or not:<br />

<details><summary>English (Inglês)</summary>
<h2>What doesn't work?</h2>
Apple AirDrop<br />
HDMI (TV and Audio Out) - This is tricky, because the HDMI output of this notebook model is connected directly to the Geforce 1650m which is not supported by the operating system (MacOS Monterey) but the digital audio SEEMS to be supported, but needs more research and testing is currently not working.<br /><br />

<h2>What works?</h2>
<h2>TOUCHPAD (Working Perfectly, with Gestures too!!)</h2>
iGPU (Intel UHD 630)<br />
nVme controller<br />
Sata Controller<br />
Audio<br />
Network Controllers (ETH and WiFi)<br />
AirDrop<br />
USB ports (including 3.1)<br />
USB-C port (4Gbps)<br />
Battery Sensor<br />
CPU Sensors (Temperature)<br />
Headphone and Microphone Input<br />
Built-in microphone<br />
Built-in Webcam<br /><br />

<h2>Keyboard Shortcuts - via Function Key (FN))</h2>
<h3>It works:</h3>
[FN]+[F4] - Sleep Mode<br />
[FN]+[F6] - Turn off the LCD<br />
<b>[FN]+[F7] - Turn Off/On Touchpad (WORKING NOW)</b><br />
[FN]+[F8] - Disable the audio (mute)<br />
[FN]+[F9] - Decreases keyboard backlight<br />
[FN]+[F10] - Increases the keyboard backlight<br />
[FN]+[F11] - Increases screen brightness<br />
[FN]+[F12] - Decreases screen brightness<br />
[FN]+[Pg Up] - Launch the Apple Music App<br />
[FN]+[Left/Right Arrow] Decrease/Increase Screen Brightness<br />
[FN]+[Down/Up Arrow] Decrease/Increase Volume<br />
<h3>Doesn't Work:</h3>
[F3] - Toggle WiFi on and off<br />
[F5] - Switch Display (Internal / External Video (HDMI))></details>

<details><summary><em>Operating system used:</em></summary>
<h4>This method was only tried with the restore mode, so boot from the Pendrive with the tool provided in the package</h4><br />
The MacOS Monterey package was used, with the latest version downloaded directly from the Apple repositories, <b>12.1</b> (BaseSystem.dmg - used only for initial booting, all installation is done over the internet)<br / ></details>

<h2> TODO: AirDrop (Troca da Placa de Wi-Fi) e HDMI (com Dongle USB)<br />
  TODO: Airdrop (Wi-Fi Board Change) and HDMi (USB/USB-C Dongle)</h2>
  
  Agradecimentos
  <a href="https://github.com/SaeedHaidar">SaeedHaidar</a> (EFI original)
  <a href="https://github.com/sostenesg7/Nitro5-an517-51-55NT-hackintosh-EFI">sostenesg7
  <a href="https://olarila.com">Mald0n</a> (Olarila Vanilla Hackintosh - Onde aprendi a dar patch direto na DSDT)
  <a href="https://hackintoshvanilla.com/">Gabriel Luchina</a> (Universo Hackintosh)
  
  #EUNAOUSOHACKINTOSHMODIFICADO #hackintoshvanilla
  
  




