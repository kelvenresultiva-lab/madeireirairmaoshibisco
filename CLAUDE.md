# Contexto do projeto

Site institucional da **Madeireira Irmãos Hibisco** (Contagem/MG). Continue a partir do código existente. Não refaça do zero e não converta para outro framework sem solicitação.

## Empresa (dados do perfil no Google Maps, 13/11/2026)

- Endereço: Av. Retiro dos Bandeirantes, 931 – Retiro, Contagem – MG, 32050-700. Coordenadas -19.8433669,-44.150408 (rotas Google Maps/Waze e mapa embutido ativos).
- Telefone (31) 3356-1512, fixo com WhatsApp confirmado pelo usuário (wa.me/553133561512).
- Horário: seg. a sex. 8h–17h, sáb. 8h–12h, dom. fechado.
- Ainda sem e-mail ou Instagram. Não inventar.

## Design aprovado

- Fundo branco, textos pretos e detalhes discretos em marrom madeira (#542a11) com destaque laranja (#e0912f). Pouco verde.
- DM Sans é a fonte principal; Playfair Display em destaque na hero.
- Cabeçalho branco, logo, navegação e botão de orçamento. Altura 86px desktop e 74px celular. Menu 15px/500 (14px até 1180, 13px até 1050, 17px no menu aberto do celular, itens com padding 7px).
- Logo: a empresa não tem arquivo de logo. A marca é em HTML: símbolo do tronco cortado (`assets/logo-hibisco-icone.svg`, também favicon) + "IRMÃOS" laranja / "HIBISCO" marrom (creme no rodapé). Estilos em style#logo-hibisco. Trocar se o cliente enviar a logo dele.
- Fotos coloridas, sem sombreado ou degradê branco. Hero com véu escuro discreto para legibilidade (style#hero-legivel).
- Cards de produtos alinhados, com fresta de 6px; no celular, descrição em 2 linhas e títulos balanceados.
- Sobre a empresa com duas imagens sobrepostas e texto ao lado.
- Seção #inspiracoes: manter o design do mosaico. Fotos de espécies comuns (eucalipto, cedrinho, pinus, angelim, ipê) em assets/madeiras/especies, ilustrativas e não confirmadas pela empresa.
- Rodapé marrom #542a11, textos creme #f6ecdc, destaques laranja.
- Celular: letras maiores (~2px acima do template), selo .about-signature escondido, hero alta (90svh).
- Animações de entrada (style#animacoes + script com barra .progresso).
- Não restaurar as seções removidas: serviços, processo, faixa de categorias e CTA com deck.

## Seções e navegação

`#inicio`, `#sobre`, `#produtos`, `#por-que-escolher`, `#inspiracoes`, `#perguntas-frequentes`, `#localizacao` e rodapé.

## Funcionalidades

- Menu expansível no celular com aria-expanded e fechamento ao selecionar uma seção ou apertar Escape.
- Botões de orçamento (cabeçalho, hero, FAQ, rodapé, cotação das linhas/madeiras) abrem DIRETO o WhatsApp da empresa, sem formulário (função openQuote()). Com madeira/linha, a mensagem cita o nome. O diálogo #contact-modal ficou no HTML mas não é aberto.
- Cards abrem diálogo de produto.
- FAQ usa details/summary.

## Trabalho no código

HTML, estilos e script estão em `index.html`. Há regras CSS acumuladas; as regras finais prevalecem. Imagens locais em `assets/`. Não remover arquivos sem checar referências no HTML e CSS.

Para conferir, rode `npm run dev` e verifique desktop e celular. Não adicionar estatísticas, depoimentos, certificações ou promessas comerciais sem confirmação do usuário.

## GitHub/Vercel

Remoto https://github.com/kelvenresultiva-lab/madeireirairmaoshibisco (branch main). vercel.json (estático, sem build) + .vercelignore (server.mjs, CLAUDE.md, IMAGENS.md). Prévia do WhatsApp: Open Graph aponta para https://madeireirairmaoshibisco.vercel.app/assets/og-hibisco.jpg — se o domínio final mudar, trocar og:url/og:image.
