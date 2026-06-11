# 🧪 Guia de Variantes e Versões do Proton

O Proton não é apenas "uma coisa só". Existem diversas compilações (ports) da comunidade e da Valve, cada uma com um objetivo técnico diferente.

## 🛠️ O que é o Protontricks?
Antes de mexer nas versões, você precisa do **[Protontricks](https://github.com/Matoking/protontricks)**. 
Ele é um wrapper do famoso *Winetricks*. Ele permite que você execute comandos e instale dependências (como fontes, DirectX, bibliotecas .NET ou DLLs proprietárias)
**dentro do prefixo de um jogo específico**. É a ferramenta definitiva para consertar jogos que não abrem ou que precisam de um componente extra que não vem no Proton padrão.

---

## 🔀 Flavors (Ports) do Proton

| Nome | Foco | Público-Alvo |
| :--- | :--- | :--- |
| **Proton GE** | Compatibilidade antecipada e codecs. | Usuários que querem rodar jogos sem erros de vídeo/áudio. |
| **Proton CachyOS** | Otimização extrema de performance. | Usuários que buscam cada FPS extra (patch de schedulers). |
| **Proton TKG** | Customização máxima (compilação). | Usuários que querem testar patches específicos de Wine/Kernel. |
| **Boxtron** | Rodar jogos DOS/Win32 via DOSBox. | Jogos retrô (não usa Wine, usa DOSBox). |
| **Luxtorpeda** | Natividade. | Tenta rodar jogos usando engines nativas Linux (ex: *OpenMW*). |
| **Steam Tinker Launch** | "Canivete suíço". | Usuários que precisam configurar *tudo* externamente (modding, scripts). |

*(Nota: Proton EM, DW, Roberta e outros são variações de nicho ou projetos experimentais de compatibilidade que seguem filosofias similares aos citados acima.)*

---

## 📈 Evolução do Proton (Versões Valve)

A Valve segue um ciclo onde o *Experimental* recebe as novidades primeiro e, eventualmente, elas se tornam parte de uma versão estável.

1. **Proton 1.0 - 3.x (A Era Pioneira):** Foco em DirectX 9/11 básico e estabilidade inicial.
2. **Proton 4.x - 5.x (Era DXVK):** Integração massiva do DXVK para tradução D3D11 -> Vulkan.
3. **Proton 6.x - 7.x (Era VKD3D):** Introdução do suporte D3D12 (jogos modernos).
4. **Proton 8.x - 9.x (Era Steam Deck/Consolidação):** Foco total em portabilidade, anti-cheat básico e performance.
5. **Proton 10.0:** A base estável atual, altamente testada para o ecossistema SteamOS/Deck.
6. **Proton 11.0 / Experimental:** O "Bleeding Edge". Onde novas APIs de áudio e correções de dia zero aparecem primeiro.

**Dica de ouro:** Se o jogo é lançamento, use o **Experimental**.
Se o jogo é antigo e estável, use a **versão 10.0**.
Se o jogo tem problemas de vídeo (tela preta), o **GE-Proton** é quase sempre a solução.

---

## 🏆 Exemplos de Onde Usar

* **GE-Proton:** Indispensável para jogos com cutscenes em formatos proprietários (ex: *Persona 5 Royal* ou jogos da Capcom).
* **Proton CachyOS:** Notável em jogos competitivos CPU-bound onde o scheduler do kernel faz diferença (ex: *Counter-Strike 2* ou *Dota 2*).
* **Steam Tinker Launch:** Essencial para jogos que exigem modding complexo antes de abrir (ex: *Skyrim* ou *Fallout* com muitos mods externos).
