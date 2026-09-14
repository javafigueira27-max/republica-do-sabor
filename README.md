# República do Sabor - Sistema Completo (Público + Admin)

Sistema web completo e profissional para o restaurante **República do Sabor**, localizado no Kilamba, Quarteirão F, Feira do F, Luanda, Angola.

---

## 🎨 Identidade Visual (Estilo Samacaca)

O website público possui uma identidade visual única e moderna inspirada na cultura angolana e no tradicional tecido **Samacaca**:
- **Cores principais**: Amarelo Dourado (`#E5B80B` / `#D4AF37`), Vermelho Vivo (`#C84B31`), Preto Carvão (`#111319`) e Branco (`#FFFFFF`).
- **Design**: Focado na gastronomia tradicional angolana (Muamba, Mufete, Grelhados), responsivo em telemóveis, tablets e computadores.

---

## 📁 Estrutura Unificada do Projeto

```text
republica_do_sabor/
├── public/                    # Website Público (Área do Cliente)
│   ├── css/
│   │   └── samacaca-style.css # Estilos Samacaca, Animações & Layout
│   ├── js/
│   │   ├── cart.js            # Carrinho, Validação de Zonas e WhatsApp
│   │   ├── gallery-lightbox.js# Lightbox interativo de fotos
│   │   └── public-app.js      # Consumo de APIs e pesquisa em tempo real
│   ├── index.html             # Página Inicial (Hero, Destaques, Sobre, Galeria, Como Encomendar)
│   ├── cardapio.html          # Cardápio Completo com Filtros e Pesquisa
│   ├── galeria.html           # Galeria de Fotografias com Lightbox
│   ├── sobre.html             # História e Valores da República do Sabor
│   └── contactos.html         # Horários, Localização e Contacto WhatsApp
│   └── images/                # Organização de Imagens (pratos, banners, galeria, logo)
├── admin/                     # Painel Administrativo (Acesso Restrito)
│   ├── css/admin.css
│   ├── js/ (api.js, auth-guard.js, admin-main.js)
│   ├── login.html             # Login admin (admin / Sabor2026!)
│   ├── dashboard.html         # Visão geral e estado do restaurante
│   ├── pratos.html            # Gestão do Cardápio
│   ├── categorias.html        # Gestão de Categorias
│   ├── banners.html           # Banners Promocionais
│   ├── galeria.html           # Gestão de Fotografias
│   ├── restaurante.html       # Dados Institucionais & WhatsApp
│   ├── encomendas.html        # Gestão de Pedidos
│   ├── configuracoes.html     # Logótipo e Marca
│   └── seguranca.html         # Alteração de Palavra-passe
├── server/
│   └── server.js              # Servidor Node.js (REST API, Sessions, Uploads, Rotas Públicas)
├── data/                      # Persistência em Ficheiros JSON
│   ├── admin.json, pratos.json, categorias.json, banners.json,
│   └── galeria.json, restaurante.json, configuracoes.json, encomendas.json
├── package.json
└── README.md
```

---

## 🔑 Credenciais & Endereços de Acesso

- **Área Pública (Cliente)**: [http://localhost:3000](http://localhost:3000)
- **Painel Administrativo**: [http://localhost:3000/admin](http://localhost:3000/admin)
- **Utilizador Admin**: `admin`
- **Palavra-passe Inicial**: `Sabor2026!`

---

## 🚀 Como Executar o Sistema

### 1. Instalar Dependências
```bash
npm install
```

### 2. Iniciar o Servidor Único
```bash
node server/server.js
```

---

## 🛍️ Carrinho de Compras & Encomendas WhatsApp

- **Zonas de Entrega Permitidas**: Exclusivamente **Kilamba** e **Kappa Kappa**.
- **Bloqueio de Zonas Inválidas**: Se o cliente tentar selecionar outra zona, o sistema bloqueia o pedido com a mensagem oficial:
  > *"Pedimos desculpa, mas neste momento as nossas entregas estão disponíveis apenas para Kilamba e Kappa Kappa."*
- **Bloqueio de Pratos Indisponíveis**: Pratos desativados pelo administrador não podem ser adicionados ao carrinho.
- **Envio Automático**: Regista a encomenda no painel admin (`/api/encomendas`) e abre o WhatsApp com a mensagem formatada para o número configurado pelo administrador.

---

## 🧪 Testes de Integração Realizados

Todos os 10 testes de integração entre o **Painel Admin** e o **Website Público** foram realizados com 100% de sucesso.
- Alteração de nomes, preços e disponibilidade de pratos em tempo real.
- Criação de novas categorias e exibição no filtro do cardápio.
- Atualização de banners e fotografias da galeria.
- Alteração do número de WhatsApp nas configurações e integração nos pedidos.
- Bloqueio de encomendas para zonas fora de Kilamba e Kappa Kappa.

---
© 2026 República do Sabor - Todos os direitos reservados.
