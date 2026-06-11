# ⚡ Dicas Avançadas e Otimização do Sistema

Se você chegou aqui, está pronto para elevar o nível do seu ecossistema Linux. Esta documentação cobre as camadas que garantem latência mínima, periféricos configurados e segurança para seus saves.

---

## 🏎️ Latência e Input Lag (Compositor Bypass)
O "Compositor Bypass" (ou *Unredirect Fullscreen Windows*) é uma técnica onde o ambiente gráfico (GNOME, KDE, etc.) para de processar a janela do jogo, entregando o controle total da tela diretamente para a GPU.
* **Wayland:** Já faz isso nativamente de forma muito eficiente, eliminando a necessidade de configurações complexas.
* **X11:** Você pode precisar habilitar "Unredirect Fullscreen" nas configurações do seu compositor (como no KWin ou Picom) para garantir que o compositor não tente "redesenhar" o frame que o jogo já renderizou, reduzindo o *input lag*.

## 💾 Gestão de Saves: [Ludusavi](https://github.com/mtkennerly/ludusavi)
Jogos no Linux rodam dentro de prefixos isolados (pastas de Wine/Proton). Se você deletar o jogo ou formatar o sistema sem um backup, seus saves podem ser perdidos.
* **O que faz:** O Ludusavi detecta automaticamente onde estão os saves de jogos da Steam, Epic, GOG e até emuladores, permitindo backups manuais ou automatizados.
* **Por que usar:** É a ferramenta mais robusta para migrar jogos entre diferentes distros sem perder o progresso.

## 🖱️ Periféricos: Controle Total
Configurar mouses e teclados gamer não precisa ser um pesadelo sem software nativo.
* **[OpenRazer](https://openrazer.github.io/):** O driver definitivo para dispositivos Razer. Permite controlar efeitos de iluminação e DPI via terminal ou interfaces gráficas.
* **[Piper](https://github.com/libratbag/piper) / [Libratbag](https://github.com/libratbag/libratbag):** Uma interface gráfica fantástica para configurar mouses gamer de diversas marcas (Logitech, SteelSeries, etc.). Você pode ajustar botões, DPI e perfis de LED que ficam salvos diretamente na memória do mouse (*onboard memory*).

## 🎮 Controles (DualSense / Xbox)
O kernel Linux possui drivers nativos excelentes, mas o comportamento pode variar:
* **Xbox:** O suporte é *plug-and-play*. Se usar via Bluetooth, o **[xpadneo](https://github.com/atar-axis/xpadneo)** é altamente recomendado, pois corrige erros de mapeamento e melhora a estabilidade da conexão.
* **DualSense (PS5):** Funciona perfeitamente na Steam. Para garantir o suporte às funções de gatilho e rumble em jogos fora da Steam, o driver `hid-playstation` (já presente no kernel moderno) é o responsável.
* **Dica:** Utilize o menu "Big Picture" da Steam para calibrar zonas mortas e remapeamento de botões de qualquer controle.

---

## 🛠️ Resumo Técnico para Power Users

| Tecnologia | Finalidade | Impacto na Performance |
| :--- | :--- | :--- |
| **Compositor Bypass** | Reduz Input Lag | Alto |
| **Ludusavi** | Segurança de Dados | N/A |
| **Libratbag** | Customização de Hardware | N/A |
| **xpadneo** | Estabilidade Bluetooth | Baixo |
