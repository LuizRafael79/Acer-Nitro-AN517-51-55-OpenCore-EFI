# Acer-Nitro-AN517-51-55-OpenCore-EFI (OpenCore 0.78)
<h2>EFI OpenCore para o notebook Acer Nitro 5 AN517-51-55 (17 Polegadas, Core i5 9300H, Geforce 1650, Intel UHD 630)</h2>

Detalhamento do que funciona e não funciona<br />

<details><summary>Português do Brasil</summary>
<h2>O que não funciona?</h2>
Touchpad (Tentando fazer funcionar)<br />
HDMI (Saída para TV e Áudio) - Aqui é complicado, porque a saída HDMI desse modelo de notebook é ligada diretamente na Geforce 1650m que não é suportada pelo sistema operacional (MacOS Monterey) porém o áudio digital PARECE ser suportado, mas necessita de mais pesquisa e testes, por hora não está funcionando.<br /><br />

<h2>O que funciona?</h2>
iGPU (Intel UHD 630)<br />
Controlador nVme<br />
Controlador Sata<br />
Áudio<br />
Controladores de Rede (ETH e WiFi)<br />
AirDrop<br />
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
[FN]+[F9] - Diminui a retroiluminação do teclado<br />
[FN]+[F10] - Aumenta a retroiluminação do teclado<br />
[FN]+[F11] - Aumenta o Brilho da tela<br />
[FN]+[F12] - Diminui o Brilho da tela<br />
[FN]+[Pg Up] - Inicia o App do Apple Music<br />
[FN]+[Seta pra Esquerda/Direita] Diminui/Aumenta o Brilho da Tela<br />
[FN]+[Seta para Baixo/Cima] Diminui/Aumenta o Volume<br />
<h3>Não Funciona:</h3>
[F3] - Alternar WiFi ligado e desligado<br />
[F5] - Alternar Display (Vídeo Interno / Externo (HDMI))<br />
[F7] - Desligar o Touchpad<br /></details>

<details><summary><em>Sistema operacional usado:</em></summary>
<h4>Este método foi tentado apenas com o modo de restauração, então faça o boot pelo Pendrive com a ferramaenta disponibilizada no pacote</h4><br />
Foi usado o pacote do MacOS Monterey, com a última versão baixada diretamente dos repositórios da Apple, <b>12.1</b> (BaseSystem.dmg - usado apenas para dar o boot inicial, toda instalação é feita pela internet)</details>

<h2>EFI OpenCore for notebook Acer Nitro 5 AN517-51-55 (17 Inch., Core i5 9300h, Geforce 1650, Intel UHD 630)</h2>

Details about what Work or not:<br />

<details><summary>English (Inglês)</summary>
<h2>What doesn't work?</h2>
Touchpad (Trying to make it work)<br />
HDMI (TV and Audio Out) - This is tricky, because the HDMI output of this notebook model is connected directly to the Geforce 1650m which is not supported by the operating system (MacOS Monterey) but the digital audio SEEMS to be supported, but needs more research and testing is currently not working.<br /><br />

<h2>What works?</h2>
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
[F5] - Switch Display (Internal / External Video (HDMI))<br />
[F7] - Turn off Touchpad<br /></details>

<details><summary><em>Operating system used:</em></summary>
<h4>This method was only tried with the restore mode, so boot from the Pendrive with the tool provided in the package</h4><br />
The MacOS Monterey package was used, with the latest version downloaded directly from the Apple repositories, <b>12.1</b> (BaseSystem.dmg - used only for initial booting, all installation is done over the internet)<br / ></details>





