# Nano ORYKSA

[![English](https://img.shields.io/badge/English-30363d?style=for-the-badge)](README.md) [![Português](https://img.shields.io/badge/Portugu%C3%AAs-0891b2?style=for-the-badge)](README.pt.md) [![Español](https://img.shields.io/badge/Espa%C3%B1ol-30363d?style=for-the-badge)](README.es.md) [![Français](https://img.shields.io/badge/Fran%C3%A7ais-30363d?style=for-the-badge)](README.fr.md)

**A IA offline da app móvel da ORYKSA.**

Quando o telemóvel perde o sinal - num avião, num túnel, numa cave - o assistente da ORYKSA
não fica às escuras. Uma versão mais pequena dela, a **Nano ORYKSA**, assume a partir de
dentro do telemóvel. Ela é mais limitada do que a ORYKSA com quem falas online, mas
leva a memória consigo: o teu perfil, os teus serviços, os teus preços, o teu horário
de funcionamento e todo o teu Brain.

Este repositório aloja os ficheiros do modelo que a app descarrega. Nada aqui corre num
servidor: tudo foi pensado para correr no próprio telemóvel.

Desenvolvido por **Weslley Harakawa** - [ORYKSA](https://oryksa.com)

---

## O que a Nano ORYKSA faz sem ligação

- Responde sobre o teu negócio, a partir da memória sincronizada com o telemóvel
- Anota tudo o que lhe pedires para mudar e executa-o assim que voltares a ter ligação
- Conversa contigo e ajuda-te a acalmar quando estás stressado ou ansioso
- Dá números de emergência e primeiros socorros básicos, sem qualquer ligação

## O que ela não consegue fazer offline

- Ler novas mensagens de clientes (essas vivem no servidor)
- Marcar compromissos ou alterar a tua conta (vão para uma fila)
- Pesquisar na web

Ela diz-o com clareza em vez de fingir. Tudo o que precisa do servidor fica numa fila
e é executado, um a um, assim que o telemóvel volta a ter ligação.

---

## Como a app escolhe um cérebro

| Telemóvel | O que corre | Descarga |
|---|---|---|
| iPhone 15 Pro e mais recentes, iOS 26 com Apple Intelligence | o modelo que a Apple já inclui no iOS | **nenhuma** |
| iPhones mais antigos e Android | o modelo publicado neste repositório | opcional, a pedido |
| Qualquer outro | consulta da memória, sem modelo nenhum | nenhuma |

A app da ORYKSA nas lojas **nunca inclui um modelo**. Fica pequena. A IA offline
só é descarregada se o dono a pedir, e pode ser apagada a qualquer momento para libertar
espaço.

## A memória

Antes de o sinal cair, a app guarda uma cópia de tudo o que a Nano ORYKSA precisa de
saber. É texto, medido em quilobytes, obtido de `GET /api/app/offline-pack`
e atualizado automaticamente sempre que a app abre ou volta ao ecrã.

## Versões

Os ficheiros do modelo são publicados como ficheiros de versão (release assets). A app lê o endereço de descarga
do backend da ORYKSA, por isso o modelo pode ser trocado ou desligado sem
publicar uma nova versão da app.

| Ficheiro | Modelo | Tamanho | Formato |
|---|---|---|---|
| `oryksa-nano.gguf` | Gemma 3 1B Instruct (Q4_K_M) | 778 MB | GGUF |

## Licença dos modelos

Os pesos dos modelos publicados aqui mantêm a licença dos seus autores originais.
O Gemma é distribuído sob os [Gemma Terms of Use](https://ai.google.dev/gemma/terms)
da Google. Usar este repositório implica aceitar esses termos.

## Sobre o autor

**Weslley Harakawa** - Fundador da ORYKSA AI e Chief Innovation Officer da Harakawa Tech. Em Lisboa, Portugal. Especialidades: inteligência artificial, desenvolvimento web e mobile, tokenização em blockchain. Formação: University of the People.

- Website: https://harakawa.tech
- LinkedIn: https://www.linkedin.com/in/weslleyharakawa/
- Instagram: https://www.instagram.com/weslley.harakawa
- ORYKSA AI Employees: https://oryksa.com (X: https://x.com/oryksa, Instagram: https://www.instagram.com/oryksaai, YouTube: https://www.youtube.com/@ORYKSA)

O nome, a marca e a app ORYKSA são propriedade de Weslley Harakawa.
