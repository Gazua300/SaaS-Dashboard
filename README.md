# 📈 Análise e Painel de Controle SaaS — Central de Inteligência de Negócios

[![Live Demo](https://img.shields.io/badge/Live_App-Experimente-2ea44f?style=for-the-badge&logo=vercel)](https://dashboard-project-nu-one.vercel.app/)
[![Portfolio](https://img.shields.io/badge/Autor-Flamarion_França-007acc?style=for-the-badge&logo=render)](https://meu-porfolio-two.vercel.app/)

> **Núcleo do Ecossistema:** O *Painel de Controle SaaS* funciona como o mecanismo centralizado de Business Intelligence (BI) da plataforma. Ele agrega fluxos de receita, volumes de transações, crescimento de usuários da plataforma e desempenho dos comerciantes gerados em toda a plataforma. **[Meu Delivery](https://meu-delivery-eight.vercel.app/)** and **[Meu Delivery Provedor](https://meu-delivery-provedor.vercel.app/)**, powered by **Meu Delivery Server**.

---

## ⚡ Demonstração interativa em tempo real

Explore as análises da plataforma e os controles de gerenciamento diretamente no seu navegador:

* 🌐 **Applicação SaaS em tempo real:** [https://dashboard-project-nu-one.vercel.app/](https://dashboard-project-nu-one.vercel.app/) 
* 🛒 **Aplicativo para clientes em tempo real (Fonte de dados):** [https://meu-delivery-eight.vercel.app/](https://meu-delivery-eight.vercel.app/)
* 💼 **Portfólio do Desenvolvedor:** [https://meu-porfolio-two.vercel.app/](https://meu-porfolio-two.vercel.app/)

🔑 **Credenciais de acesso à demonstração:**
* **Admin 1:** `admin1@example.com` | 
* **Admin 2:** `admin2@example.com` | Todas as senhas já vem como padrão no input
* **Admin 2:** `admin2@example.com` | 

> 💡 **Fluxo de teste sugerido:** Faça login com uma das credenciais acima, navegue pelo painel de análise em tempo real, teste a alternância de internacionalização em tempo real (`i18next`), examine os módulos de gerenciamento de lojistas e clientes, e teste os formulários de configuração validados por esquema.
---

## 🌟 Destaques Técnicos e Decisões de Engenharia

Desenvolvido com **Vite**, **React**, **TypeScript**, **Tailwind CSS** e **Zod**, este painel demonstra como estruturar ferramentas de inteligência corporativa prontas para produção, contando com rigorosa segurança de tipos, sistemas de interface modulares e prontidão para uso global:

* **⚡ Infraestrutura otimizada com Vite + Tailwind:** Oferece pacotes (bundles) de tamanho reduzido, *Hot Module Replacement* (HMR) instantâneo e uma arquitetura de layout responsivo baseada em classes utilitárias (*utility-first*).
* **🛡️ Validação de formulários e esquemas com segurança de tipos (*type-safe*):** Utiliza **React Hook Form** em conjunto com a inferência de esquemas do **Zod** para garantir uma verificação rigorosa de dados em tempo de execução e um tratamento de erros robusto nos painéis de configuração da plataforma.
* **🌐 Internacionalização (i18n) de nível corporativo:** Suporte para alternância de idioma em tempo real (inglês e português) por meio do `i18next`, com carregamento modular de namespaces de tradução.
* **🎨 Sistema de design escalável:** Componentes de interface (UI) reutilizáveis ​​e acessíveis, construídos com **Lucide React** e abstrações do Tailwind CSS, assegurando consistência visual em visualizações analíticas complexas.
* **📊 Agregação de dados do ecossistema:** Desenvolvido para ingerir, processar e exibir, em tempo real, volumes de pedidos, acompanhamento financeiro e métricas de desempenho da plataforma.

---

## 🏛️ Arquitetura de Ecossistema e Agregação de Dados

```text
  ┌───────────────────────────┐         ┌───────────────────────────┐
  │   Meu Delivery (Cliente)  │         │   Meu Delivery Provedor   │
  │  (Transações de clientes) │         │  (Operações com Lojistas) │
  └─────────────┬─────────────┘         └─────────────┬─────────────┘
                │                                     │
                └──────────────────┬──────────────────┘
                                   │
                                   ▼
                      ┌───────────────────────────┐
                      │    Meu Delivery Server    │
                      │     (API centralizada)    │
                      └────────────┬──────────────┘
                                   │
                                   ▼
                      ┌───────────────────────────┐
                      │  Painel de Controle SaaS  │
                      │ (Central de Análise e BI) │
                      └───────────────────────────┘