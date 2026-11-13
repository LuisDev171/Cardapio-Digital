# Cardápio Digital

Cardápio online instalável no celular (PWA). O cliente escolhe os itens, informa nome, endereço e pagamento, e o **pedido chega pronto no WhatsApp da loja**.

Feito por **Luis Dev** · WhatsApp (12) 99249-8702 · @luisrlq171

## Recursos
- Cardápio por categorias com preços e descrições
- Carrinho com total, taxa de entrega e opção de retirada
- Forma de pagamento (Pix, cartão na entrega ou dinheiro com troco) e observações
- Pedido formatado enviado direto para o WhatsApp da loja
- Área do dono para marcar itens como **esgotados** (protegida por senha)
- Instalável no Android e no iPhone, sem loja de aplicativos
- Sem dependências e sem etapa de build: HTML, CSS e JavaScript puros

## Como personalizar para um cliente
Tudo fica no começo do script do `index.html`:

```js
var CONFIG = {
  nome: 'Burger Demo',
  slogan: 'Hambúrguer artesanal feito na hora',
  whatsapp: '5512992498702',   // só números, com 55 e DDD
  horario: 'Todos os dias, das 18h às 23h',
  taxaEntrega: 6,              // 0 para entrega grátis
  pinDono: '1234'              // troque a senha da Área do dono
};
```
O cardápio está na lista `MENU` logo abaixo: categoria, nome, descrição, preço e um emoji por item.

## Como rodar localmente
```bash
python3 -m http.server 8000
# abra http://localhost:8000
```

## Publicar (GitHub Pages)
1. Suba estes arquivos em um repositório
2. **Settings > Pages > Deploy from a branch > main / (root)**
3. Abra o link no celular e use "Adicionar à tela inicial"

Ao alterar qualquer arquivo, troque o número da versão em `sw.js` (`VERSION`) para o celular receber a atualização.

## Observações
- Os itens esgotados e o carrinho ficam salvos no próprio aparelho.
- Esta é uma demonstração: troque o nome, o WhatsApp e o cardápio antes de entregar a um cliente.
- A senha da Área do dono fica no código. Ela evita mexidas acidentais, mas não é segurança forte.
