# Desafio Semana 3 - Dados Avançados (Metafields + Metaobjetos + Slider Dinâmico)

Este repositório contém a solução do desafio técnico da Shakers focado na estruturação e consumo de dados complexos no Shopify, utilizando Metaobjetos e Metafields para criar um slider de produtos dinâmico.

## 📖 O que são Metafields e Metaobjetos?

- **Metafields**: São campos personalizados que permitem estender as funcionalidades de objetos padrão do Shopify (como Produtos, Coleções ou Clientes), armazenando informações adicionais que não existem nativamente no painel administrativo.
- **Metaobjetos**: São estruturas de dados personalizáveis que permitem criar novos modelos de informação dentro da loja. Funcionam como "mini bancos de dados" onde você define campos específicos para agrupar informações relacionadas em uma única entidade.

## 🎥 Demonstração em Vídeo

Assista ao vídeo demonstrativo mostrando a configuração no Admin, o código e o slider funcionando: [Link do Vídeo aqui]

## 🚀 O que foi implementado

- **Metaobjeto Customizado**: Criação do objeto `product_with_banner` com campos de referência de produto e imagem (file)
- **Metafield de Lista**: Implementação de um Metafield de produto (`related_products_with_banner`) do tipo lista de Metaobjetos.
- **Section Dinâmica**: Desenvolvimento da section `sections/metaobject-slider.liquid` com seleção de produto via schema.
- **Lógica Liquid Avançada**:
  - Uso do método `.value` para acessar os dados dos Metafields.
  - Utilização de `all_products` para capturar objetos completos de produtos via handle.
  - Validação condicional para garantir que o HTML só seja renderizado se houver dados disponíveis.
- **Slider Interativo**: Implementação do Swiper via CDN conforme os requisitos.
- **Organização de Assets**: Separação correta de CSS e JS nas pastas de assets.

## 🛠️ Configuração do Ambiente

### 1. Criar o Metaobjeto

1. No painel Shopify, vá em **Configurações > Dados Personalizados**.
2. Crie um novo **Metaobjeto** chamado `product_with_banner`.
3. Adicione dois campos obrigatórios:
   - **Produto**: do tipo `Product reference`.
   - **Banner**: do tipo `File` (imagem).

### 2. Criar o Metafield de Produto

1. Vá em **Dados Personalizados > Produtos**.
2. Crie uma definição com o nome `related_products_with_banner`.
3. Selecione o tipo **Metaobject reference** e marque **Lista de entradas**.
4. Referencie o Metaobjeto criado no passo anterior.

### 3. Associar Dados ao Produto

1. Cadastre pelo menos 2 entradas no Metaobjeto
2. Em um produto específico, acesse a seção de Metafields e selecione as entradas cadastradas.

## 👥 Como testar localmente

1. **Clonar o repositório:**
   ```bash
   git clone https://github.com/DaniloSreis/shakers-semana-3-dados-avancados.git
   ```

2. **Acessar a branch:**
   ```bash
   git checkout feat/metaobject-slider
   ```

3. **Rodar Shopify CLI:**
    ```bash
    shopify theme dev
    ```

## 🔗 Links de Entrega
- **Pull Request:**
- **Vídeo do Desafio:**
