## 🎮 Distros Focadas em Games (Gaming-First)
A lista não carrega uma ordem especifica do melhor pro pior (exceto o SteamOS que é definitivamente a cereja do bolo)
estou apenas apresentando algumas distros com uma breve descrição.

### 1. SteamOS (Versão 3.x)
* **Ponto Forte:** A experiência definitiva de console para PC. Interface imersiva, gestão unificada pela Steam e otimização extrema de bateria e performance via Gamescope.
* **Suporte/Desenvolvedor:** Valve Corporation.
* **Compatibilidade:**
  * **Handheld:** Nativo (Projetado para o Steam Deck).
  * **AMD:** Excelente (Foco principal de desenvolvimento).
  * **NVIDIA:** Ruim/Inexistente (A Valve não otimiza o SteamOS oficialmente para chips Nvidia no momento).

### CachyOS
* **Ponto Forte:** Performance extrema e otimização de baixo nível. Utiliza um kernel com patches customizados (schedulers como BORE/Cachy) e pacotes compilados especificamente para extrair até o último FPS do hardware.
* **Suporte/Desenvolvedor:** CachyOS Team.
* **Compatibilidade:**
  * **Handheld:** Muito Boa (Lançaram recentemente a edição CachyOS Handheld).
  * **AMD:** Excelente (Drivers Mesa bleeding-edge).
  * **NVIDIA:** Excelente (Instalação fácil do driver proprietário via instalador GUI).

### Bazzite
* **Ponto Forte:** É a melhor alternativa atual ao SteamOS para PCs de mesa e handhelds de terceiros (como ROG Ally). Baseado no Fedora OSTree (imutável), é indestrutível e já vem com tudo pré-instalado.
* **Suporte/Desenvolvedor:** Universal Blue (Comunidade apoiada pelo ecossistema Fedora).
* **Compatibilidade:**
  * **Handheld:** Excelente (Possui imagens específicas para Ally, Legion Go e Steam Deck).
  * **AMD:** Excelente.
  * **NVIDIA:** Existe (mas não funcionou muito bem com minha RTX 3060)

### Nobara Linux
* **Ponto Forte:** Desenvolvido pelo criador do "GE-Proton", traz correções de kernel e patches do OBS Studio/Gamescope que a base Fedora demora a implementar. É a distro "pronta para jogar e fazer stream".
* **Suporte/Desenvolvedor:** Thomas Crider (GloriousEggroll) e comunidade.
* **Compatibilidade:**
  * **Handheld:** Boa (Pode exigir configuração manual da interface Steam Deck UI).
  * **AMD:** Excelente.
  * **NVIDIA:** Excelente (Instalador automatizado de drivers e detecção de hardware).

### ChimeraOS
* **Ponto Forte:** Instalação limpa que vai direto para a interface do Steam Big Picture (modo console). Funciona como um "SteamOS genérico" sem precisar da complexidade do HoloISO.
* **Suporte/Desenvolvedor:** ChimeraOS Team.
* **Compatibilidade:**
  * **Handheld:** Excelente (Suporta controles do AyaNeo, GPD, etc., nativamente).
  * **AMD:** Excelente (Foco principal).
  * **NVIDIA:** Ruim (Não suportado oficialmente pela equipe).

### Regata OS
* **Ponto Forte:** Distro brasileira com uma loja própria fenomenal (Regata OS Store) que integra instalação de jogos da Epic, EA, Ubisoft e Battle.net nativamente e com um clique.
* **Suporte/Desenvolvedor:** Marcos Geraldo e comunidade Regata OS (Brasil).
* **Compatibilidade:**
  * **Handheld:** Ok (Pode ser usado, mas é focado em Desktop/Notebook).
  * **AMD:** Excelente.
  * **NVIDIA:** Excelente (Sistema Max-Q suportado out of the box).

### Garuda Linux (Dr460nized Gaming Edition)
* **Ponto Forte:** Um Arch Linux amigável, visualmente agressivo e que já vem com Lutris, ProtonUp-Qt, Wine e todas as dependências pré-instaladas. Usa BTRFS com snapshots automáticos (se quebrar, basta reverter ao boot anterior).
* **Suporte/Desenvolvedor:** Garuda Linux Team.
* **Compatibilidade:**
  * **Handheld:** Ok.
  * **AMD:** Excelente.
  * **NVIDIA:** Excelente.

### HoloISO
* **Ponto Forte:** Tentativa da comunidade de empacotar o SteamOS 3.0 oficial do Steam Deck para qualquer PC comum.
* **Suporte/Desenvolvedor:** The Vakhovske/Comunidade.
* **Compatibilidade:**
  * **Handheld:** Excelente.
  * **AMD:** Excelente.
  * **NVIDIA:** Ruim (Frequentemente quebra a interface gráfica).

### PikaOS
* **Ponto Forte:** Um "Nobara, mas baseado em Ubuntu". Traz as otimizações pesadas de kernel e drivers modernos para quem prefere o ecossistema `apt` ou `dpkg`.
* **Suporte/Desenvolvedor:** PikaOS Team.
* **Compatibilidade:**
  * **Handheld:** Boa.
  * **AMD:** Excelente.
  * **NVIDIA:** Excelente.

### Batocera.linux
* **Ponto Forte:** Voltada 100% para retrogaming. Pode ser rodada de um pen drive. Transforma qualquer PC velho ou handheld chinês em um console com milhares de emuladores pré-configurados.
* **Suporte/Desenvolvedor:** Batocera Team.
* **Compatibilidade:**
  * **Handheld:** Excelente (É a principal aplicação do sistema).
  * **AMD:** Excelente.
  * **NVIDIA:** Excelente.

*(Existem outras menores como Lakka, Drauger OS, Salient OS e SparkyLinux GameOver, mas elas caem em casos de uso muito de nicho, retro-focadas ou estão desatualizadas).*

---

## 💻 Distros Gerais Usadas para Jogos (General Purpose)

Estas distribuições não são anunciadas como "distros gamer", mas são amplamente utilizadas pela comunidade gamer por sua estabilidade, acesso fácil a pacotes atualizados e vasta documentação.
No final das contas qualquer distro pode se tornar uma distro gamer se vc configurar e instalar os pacotes corretos
exceto, talvez, o Alpine linux e distros BSD.
outros sistemas como MacOS Redox OS, ReactOS e outros nem podem entrar nessa lista por serem muito distantes do linux.

### Pop!_OS
* **Ponto Forte:** A gestão de GPUs em notebooks híbridos é a melhor do mercado Linux. O System76 Scheduler ajuda na fluidez dos jogos no desktop.
* **Suporte/Desenvolvedor:** System76.
* **Compatibilidade:**
  * **Handheld:** Ruim (Interface focada em mouse/teclado).
  * **AMD & NVIDIA:** Excelente (A ISO dedicada à Nvidia é lendária por resolver dores de cabeça de instalação).

### Fedora (Workstation/KDE)
* **Ponto Forte:** O equilíbrio perfeito entre pacotes muito atualizados (bom para Mesa e Kernel) e alta estabilidade corporativa.
* **Suporte/Desenvolvedor:** Red Hat / Projeto Fedora.
* **Compatibilidade:**
  * **Handheld:** Ruim.
  * **AMD:** Excelente.
  * **NVIDIA:** Muito Boa (Requer habilitação do repositório RPM Fusion).

### BigLinux
* **Ponto Forte:** Uma obra-prima brasileira. Baseada no Manjaro, é incrivelmente polida, traz otimizações automáticas de sistema, integração com navegadores em sandbox e um painel de controle que facilita qualquer configuração de hardware.
* **Suporte/Desenvolvedor:** Bruno Gonçalves e comunidade.
* **Compatibilidade:**
  * **Handheld:** Ok (Focado em Desktop).
  * **AMD:** Excelente.
  * **NVIDIA:** Excelente (Instalação fácil via Central de Controle).

### Manjaro
* **Ponto Forte:** Acesso à AUR e pacotes recentes sem a curva de aprendizado brutal do Arch Linux puro. Possui um gerenciador gráfico de hardware (MHWD) que troca versões de kernel e drivers de GPU com um clique.
* **Suporte/Desenvolvedor:** Manjaro GmbH & Co. KG.
* **Compatibilidade:**
  * **Handheld:** Ok.
  * **AMD & NVIDIA:** Excelente.

### Ubuntu
* **Ponto Forte:** É o padrão de facto da indústria. A maioria dos jogos nativos ou ferramentas com instaladores proprietários são testados primeiro no Ubuntu. Maior quantidade de tutoriais na internet.
* **Suporte/Desenvolvedor:** Canonical.
* **Compatibilidade:**
  * **Handheld:** Ruim.
  * **AMD:** Muito Boa (Pode exigir PPAs externos para drivers atualizados).
  * **NVIDIA:** Excelente (Suporte oficial direto na aba de "Drivers Adicionais").

### Linux Mint
* **Ponto Forte:** A distribuição mais fácil para ex-usuários de Windows. Estável como uma rocha, interface familiar e amigável.
* **Suporte/Desenvolvedor:** Clement Lefebvre e Equipe Linux Mint.
* **Compatibilidade:**
  * **Handheld:** Ruim.
  * **AMD:** Boa (Baseia-se em versões mais antigas do Ubuntu, pode não ter a melhor performance em placas recém-lançadas sem atualização manual).
  * **NVIDIA:** Excelente (Usa o mesmo gestor de drivers do Ubuntu).

### Arch Linux
* **Ponto Forte:** Você monta o sistema do zero. Acesso à AUR (Arch User Repository) significa que toda ferramenta ou launcher obscuro de jogos será encontrado lá com um comando.
* **Ponto Fraco:** Distro mais dificil de instalar e manter da lista.
* **Suporte/Desenvolvedor:** Comunidade Arch Linux.
* **Compatibilidade:**
  * **Handheld:** Excelente (Se você souber instalar os pacotes certos como `gamescope-session`).
  * **AMD & NVIDIA:** Excelente (Você instala os drivers de última geração manualmente).

### Artix Linux
* **Ponto Forte:** Todo o ecossistema rápido e atualizado do Arch, acesso total à AUR, mas sem a imposição do `systemd`. Para power users que preferem init systems como OpenRC, runit ou s6, entregando um sistema base mais leve para focar recursos nos jogos.
* **Suporte/Desenvolvedor:** Artix Linux Team.
* **Compatibilidade:**
  * **Handheld:** Ok (Configuração 100% manual).
  * **AMD & NVIDIA:** Excelente (Pacotes diretos dos repositórios Arch/Artix).
