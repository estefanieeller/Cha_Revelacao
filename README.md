# 🍼 Chá Revelação Interativo

Um Web App interativo, responsivo e em tempo real desenvolvido para engajar os convidados em um evento de Chá Revelação.
A aplicação permite que familiares e amigos votem no sexo do bebê, deixem recados amorosos, tirem fotos instantâneas estilo Polaroid e acompanhem um placar ao vivo das brincadeiras do evento.

## 🌟 Funcionalidades

*   **📊 Votação em Tempo Real:** Convidados escolhem entre "Francisco 💚" e "Celina 💜". O placar e a barra de progresso são atualizados instantaneamente na tela de todos usando Firebase Firestore.
*   **💌 Mural de Recados:** Um espaço para mensagens de carinho aos pais e ao bebê, com feed rolável e atualizado na hora.
*   **📸 Câmera Instax (Mural de Fotos):** Os convidados podem abrir a câmera nativa do celular direto do site, tirar uma foto e adicionar uma legenda. As fotos aparecem em um feed com design de Polaroid.
    *   *✨ Destaque Técnico:* Para otimizar o limite de tráfego do Firebase, o upload inclui um algoritmo de **compressão de imagem no lado do cliente** usando a `Canvas API` nativa do HTML5, reduzindo fotos de múltiplos Megabytes para poucos Kilobytes antes do envio.
*   **🏆 Placar das Brincadeiras (Modo Juiz):** Um dashboard para acompanhar a pontuação dos papais durante os desafios do chá.
    *   *🔐 Modo Juiz:* Botão protegido por senha (`DP@CF`) que libera um painel de administração (botões de +1 e -1) para pontuar as brincadeiras, computando quem é o "Campeão Geral" ao vivo.
*   **🔒 Trava de Voto Único:** Utilização de `localStorage` para impedir que os convidados votem mais de uma vez, ocultando o painel de votação e exibindo mensagens personalizadas com base na cor escolhida.
*   **🎉 Efeitos Visuais:** Disparo de confetes personalizados (nas cores Verde e Lilás) a cada interação bem-sucedida, usando a biblioteca `canvas-confetti`.

## 🛠️ Tecnologias Utilizadas

*   **Frontend:** HTML5, CSS3, JavaScript (Vanilla ES6+ Modules)
*   **Backend / Banco de Dados:** Firebase Firestore (NoSQL Realtime Database)
*   **Bibliotecas Externas:** [canvas-confetti](https://github.com/catdad/canvas-confetti)
*   **Deploy:** Vercel

## 🚀 Como Executar o Projeto

Como o projeto é construído em HTML/JS estático com Firebase no frontend, não há necessidade de Node.js ou servidores locais complexos.

1. Faça o clone do repositório:
   ```bash
   git clone [https://github.com/seu-usuario/cha-revelacao.git](https://github.com/seu-usuario/cha-revelacao.git)

⚠️ Importante: O arquivo index.html contém as chaves de acesso públicas do Firebase Firestore configuradas para este evento específico. Se você for reutilizar este código para outro projeto, lembre-se de criar o seu próprio projeto no Firebase Console e substituir o objeto firebaseConfig pelas suas credenciais.
