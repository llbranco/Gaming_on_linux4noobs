# 🐧 Guia Definitivo: Gaming on Linux for Noobs

Seja bem-vindo ao guia definitivo para quem deseja explorar o universo gamer no ecossistema Linux. Nosso objetivo é eliminar as barreiras técnicas que impedem que você aproveite seus jogos favoritos, oferecendo uma base sólida de conhecimento, desde conceitos básicos até otimizações de sistema para usuários avançados.
Se você é um recém-chegado do Windows ou um usuário avançado (*power user*), este documento serve para desmistificar os termos, ferramentas e conceitos que fazem a mágica acontecer.

> *"O Linux não é apenas para servidores; é uma plataforma de jogos poderosa e altamente customizável."*

### O que você encontrará aqui:
*   **Dicionário de Termos:** Entenda o que é Wine, Proton, Prefixes e muito mais.
*   **Guia de Tecnologias:** Links e explicações sobre os pilares da compatibilidade.
*   **Tutoriais Práticos:** Como configurar launchers, gerenciar dependências e otimizar a performance.

---

## ⚙️ Tecnologias Base

### [Wine](https://www.winehq.org/)
**"Wine Is Not an Emulator"** — É a base de todo o ecossistema. É uma camada de compatibilidade de código aberto que traduz as chamadas de sistema do Windows (APIs) para comandos que o Linux entende nativamente em tempo real. Como não há emulação de hardware, a perda de performance é praticamente nula.

### [Proton](https://github.com/ValveSoftware/Proton)
Uma versão modificada do Wine desenvolvida pela Valve (criadora da Steam) em parceria com a CodeWeavers. Ele já vem integrado à Steam e traz empacotadas ferramentas essenciais de alto desempenho como o **DXVK** e o **VKD3D-Proton**, além de correções específicas para jogos modernos. É o motor por trás do Steam Deck.
[veja mais](https://github.com/llbranco/Gaming_on_linux4noobs/blob/main/PROTON_VERSIONS.md)

### [Wayland](https://wayland.freedesktop.org/)
O protocolo de servidor gráfico moderno do Linux, projetado para substituir o antigo X11. Para jogos, ele elimina completamente o *screen tearing* sem a necessidade de V-Sync tradicional (evitando input lag), além de oferecer suporte nativo a HDR, taxas de atualização variáveis (VRR/FreeSync) e melhor gerenciamento em cenários de múltiplos monitores.

---

## 📂 Conceitos Fundamentais

### Wine / Proton Prefix (Prefixos)
Pense neles como "garrafas" ou "mini-instalações isoladas do Windows". Cada jogo ou aplicativo geralmente ganha seu próprio prefixo, que é um diretório contendo uma estrutura falsa de disco `C:\` (com pastas como `Program Files`, `Windows`, `users`) e seu próprio registro do sistema. Isso garante que as modificações e dependências feitas para um jogo não quebrem outros jogos. Na Steam, eles ficam localizados em `steamapps/compatdata/`.

### Dependências
São as bibliotecas, runtimes ou softwares adicionais que um jogo precisa para rodar perfeitamente (Ex: *Visual C++ Redistributables*, *DirectX Runtimes*, *.NET Framework*). No Linux, em vez de instaladores manuais, usamos ferramentas utilitárias para injetar essas dependências diretamente dentro do prefixo do jogo.

[APIs graficas](https://github.com/llbranco/Gaming_on_linux4noobs/blob/main/GRAPHICS_API.md)

---

## 🚀 Parâmetros de Inicialização (Launch Options)

Variáveis de ambiente ou comandos passados antes da execução do jogo para injetar melhorias de desempenho, ativar recursos ou contornar bugs.

### [Feral GameMode](https://github.com/FeralInteractive/gamemode) (`gamemoderun`)
Um daemon (serviço em segundo plano) que otimiza temporariamente o sistema operacional assim que o jogo inicia. Ele altera o governador da CPU para o modo "performance", ajusta o agendamento de processos (niceness), prioriza a GPU e pode aplicar perfis personalizados de energia.

### `%command%`
Uma variável de substituição exclusiva da Steam. Tudo o que você escreve **antes** de `%command%` altera o ambiente em que o jogo roda; o que vem **depois** é repassado como um argumento direto para o executável principal do jogo.
* *Exemplo prático:* `gamemoderun %command% -novid` (Ativa as otimizações do GameMode e pula os vídeos de introdução do jogo).

---

## 🎮 Launchers e Gerenciadores de Jogos

### [Lutris](https://lutris.net/)
Uma plataforma aberta de preservação e gerenciamento de jogos. Centraliza títulos da Steam, GOG, Epic Games, emuladores e instalações avulsas (*standalone*). Destaca-se pelos seus "scripts de instalação" criados pela comunidade, que configuram o prefixo do Wine com todas as dependências ideais de forma automatizada.

### [Heroic Games Launcher](https://heroicgameslauncher.com/)
Um launcher alternativo de código aberto, leve e elegante, focado especificamente nas lojas da **Epic Games**, **GOG** e **Amazon Games**. Possui gerenciamento nativo e simplificado de prefixos do Wine/Proton e excelente integração com o Steam Deck.

### [UMU Launcher](https://github.com/Open-Wine-Components/umu-launcher)
*Unified Linux Wine Game Launcher* — Uma ferramenta avançada criada pelos desenvolvedores do GE-Proton. Permite utilizar a runtime exata do Proton da Steam para rodar jogos que estão fora da Steam (como os do GOG ou Epic), padronizando a compatibilidade no ecossistema Linux.

### [Faugus Launcher](https://github.com/Faugus/faugus-launcher)
Um gerenciador focado na organização e execução simplificada de jogos de fontes alternativas (como repacks) ou softwares standalone, abstraindo a complexidade de configuração manual do Wine.

### [PortProton](https://github.com/Castro-Fidel/PortWINE)
Um projeto focado na usabilidade instantânea. Permite executar arquivos `.exe` com um duplo clique no gerenciador de arquivos, encarregando-se de baixar as versões necessárias do Proton, configurar scripts e otimizar o ambiente sem intervenção complexa do usuário.

---

## 🛠️ Utilitários de Gerenciamento do Proton

Versões customizadas do Proton (como o **GE-Proton** do GloriousEggroll) incluem correções rápidas de bugs e codecs de vídeo proprietários que a Valve não pode distribuir legalmente por questões de licenciamento. Para gerenciá-los facilmente, usamos:

### [ProtonUp-Qt](https://davidotek.github.io/protonup-qt/)
Interface gráfica intuitiva que permite baixar, atualizar e remover versões personalizadas do Proton (para a Steam) e Wine-GE (para Lutris e Heroic Launcher) com apenas um clique.

### [ProtonPlus](https://github.com/Vysp3r/ProtonPlus)
Uma alternativa moderna ao ProtonUp-Qt. Desenvolvido em GTK4/Libadwaita, integra-se visualmente a ambientes como o GNOME e gerencia compatibilidades para múltiplos launchers simultaneamente de forma limpa.

---

## 🔍 Compatibilidade e Consulta

### [ProtonDB](https://www.protondb.com/)
O maior banco de dados mantido pela comunidade Linux Gamer. Avalia o status de funcionamento de milhares de jogos em categorias de certificação (*Platinum, Gold, Silver, Bronze, Broken*). Se um jogo apresentar problemas, a seção de comentários dos usuários costuma conter a solução exata (ajustes de parâmetros ou dependências).

### [Are We Anti-Cheat Yet?](https://areweanticheatyet.com/)
Jogos multiplayer competitivos com anti-cheats a nível de kernel ou proprietários (como *Valorant, Call of Duty, Destiny 2*) são o maior desafio no Linux. Este site cataloga em tempo real quais jogos multiplayer são compatíveis, quais possuem suporte nativo ativado pelas desenvolvedoras e quais continuam bloqueados.

---

## 💡 Dicas Rápidas de Otimização

1. **Use o GE-Proton para vídeos corrompidos:** Se um jogo travar ou exibir barras coloridas/telas pretas em cutscenes, use o ProtonUp-Qt para baixar o *GE-Proton* mais recente e selecione-o nas propriedades do jogo.
2. **Evite partições NTFS:** O Proton e o Wine gerenciam permissões de arquivos no formato POSIX do Linux. Executar jogos a partir de um HD/SSD formatado em NTFS (padrão do Windows) causa falhas críticas de escrita e corrupção de prefixos. Prefira **ext4** ou **btrfs** para a biblioteca.
3. **Mantenha os drivers de GPU atualizados:** No Linux, para placas AMD e Intel, os drivers de vídeo fazem parte do Kernel e da biblioteca **Mesa**. Mantenha o sistema sempre atualizado para garantir os patches mais recentes do ecossistema gráfico (*RADV/ANV*).
