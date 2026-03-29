# 💡 Módulo 1: EcoSimulador (Energia)

Este projeto faz parte de um ecossistema de ferramentas para consultores de vendas. O **EcoSimulador** é uma aplicação web focada em calcular a estimativa de economia em contas de energia elétrica, utilizando uma interface limpa e feedback em tempo real para o usuário.

## 🚀 Funcionalidades

* **Cálculo Reativo:** Atualização instantânea dos resultados à medida que o usuário digita, melhorando a experiência do usuário (UX) sem a necessidade de recarregar a página.
* **Formatação Monetária Nativa:** Utilização da API `Intl.NumberFormat` para garantir a exibição correta e localizada de moedas (Padrão BRL - R$).
* **Feedback Visual e Validação:** Tratamento de erros robusto ("Early Return") para valores zerados ou inválidos, exibindo mensagens claras de orientação.
* **Design Responsivo (Mobile First):** Layout fluido construído com CSS Grid e Flexbox, adaptando-se perfeitamente de smartphones a monitores ultrawide.

## 🛠️ Tecnologias Utilizadas

* **HTML5:** Foco em semântica e acessibilidade.
* **CSS3:** Estilização pura (Vanilla CSS) sem dependências externas.
* **JavaScript (Vanilla):** Manipulação de DOM, formatação de dados e regras de negócio isoladas.

## 🧠 Arquitetura e Boas Práticas (Clean Code)

A base de código foi projetada para ser legível e fácil de manter:

* **Eliminação de "Magic Numbers":** A taxa de desconto de 10% foi extraída para uma constante global `const DISCOUNT_RATE = 0.10;`, facilitando futuras alterações na regra de negócio num único ponto.
* **Princípio da Responsabilidade Única (SRP):** As funções fazem apenas uma coisa. `formatCurrency` lida estritamente com a formatação, enquanto `calculateDiscount` foca na matemática.
* **Early Return (Retorno Antecipado):** Na função de cálculo, a validação de erro (`if (accountValue <= 0)`) é feita no início, evitando o aninhamento excessivo de blocos `if/else`.

## ⚙️ Como Executar

Este módulo não requer instalação de dependências. Basta abrir o arquivo `index.html` diretamente no seu navegador ou utilizar uma extensão como o "Live Server" no VS Code.

---
*Desenvolvido como projeto de portfólio por Adriano Luz*