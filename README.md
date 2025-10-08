
<p align="center">
  <img src="docs/logo-fiberapp.png" alt="Logo FiberAppRF" width="200">
</p>

<h1 align="center">FiberAppRF</h1>

<p align="center">
  🚀 App & Chatbot inteligente para clientes da Fiber.NET — resolva boletos e suporte sem sair do celular.
</p>

---

## 📋 Índice

- [Visão & Propósito](#visão--propósito)  
- [Funcionalidades & Demonstração](#funcionalidades--demonstração)  
- [Objetivos & Metas](#objetivos--metas)  
- [Escopo (MVP vs Futuro)](#escopo-mvp-vs-futuro)  
- [Critérios de Aceitação](#critérios-de-aceitação)  
- [Roadmap](#roadmap)  
- [Stack Tecnológica](#stack-tecnológica)  
- [Como Rodar / Instalar](#como-rodar--instalar)  
- [API IXC – Integração](#api-ixc--integração)  
- [Contribuição & Feedback](#contribuição--feedback)  
- [Licença](#licença)  
- [Autores / Responsáveis](#autores--responsáveis)  

---

## 🌱 Visão & Propósito

A **FiberNET**, como provedor de internet, enfrenta muitos chamados relacionados a cobranças ou dúvidas técnicas.  
O **FiberAppRF** nasce para empoderar o cliente com autoatendimento digital: **WhatsApp + App Android (e depois iOS)**, reduzindo o esforço para resolver problemas simples e liberando o time de suporte para questões mais complexas.

---

## 🔍 Funcionalidades & Demonstração

- Chatbot via WhatsApp: emissão de boletos, abertura/consulta de chamados, fallback humano  
- App Android: login, visualização de faturas (boleto / PIX / PDF), abertura/consulta de chamados, notificações push  
- [GIF / mockup aqui demonstrando telas iniciais]

---

## 🎯 Objetivos & Metas SMART

**Chatbot (MVP)**  
- Lançar em até 3 semanas  
- Piloto com ≥ 20 clientes  
- Resolver ≥ 80% das requisições de boleto automaticamente  

**App Android (MVP)**  
- Lançar em até 6 semanas  
- Beta com ≥ 10 usuários  
- Entregar boleto em ≤60 segundos após solicitação  

**iOS (Fase 2)**  
- Lançar em até 8 semanas após Android validado  

---

## 📦 Escopo (MVP vs Futuro)

**MVP (versão zero):**
- Chatbot: boleto, abertura/consulta de chamados  
- App Android: login, faturas, chamados, push  

**Futuro:**
- Pagamentos embutidos  
- Teste de velocidade  
- Banners / promoções dinâmicas  
- Integração com API oficial WhatsApp  
- Módulo “Indique e Ganhe”  

---

## ✅ Critérios de Aceitação (DoD)

**Chatbot concluído quando:**  
- Retorna boleto válido via CPF/contrato  
- Gera protocolo para chamado no IXC  
- Permite consultar status de chamados  
- Fallback para atendimento humano  
- Testes com 20 usuários piloto sem erro crítico  

**App Android concluído quando:**  
- Login funcional  
- Exibe faturas + links / PIX  
- Abre / consulta chamados  
- Push notificações funcionam  
- Publicado e testado com 10 usuários  

---

## 🗓 Roadmap Estimado

| Fase | Duração | Principais entregas |
|---|---|---|
| Planejamento & configuração API IXC | 1–2 semanas | Setup token, permissões, estrutura do repo |
| Chatbot MVP | 3 semanas | Bot rodando com fluxo boleto + chamado |
| App Android MVP | 6 semanas | App com telas, conexão com backend |
| Validação e ajustes | 2 semanas | Feedbacks, ajustes, correções |
| App iOS (fase 2) | 6–8 semanas | Adaptação, testes e publicação iOS |

---

## 🧰 Stack Tecnológica

- **Chatbot:** Node.js + Venom Bot / WPPConnect  
- **Backend Middleware:** Node.js (Express / NestJS) + API IXCSoft  
- **App:** Flutter (Android / iOS)  
- **Notificações:** Firebase Cloud Messaging  
- **Infraestrutura:** VPS inicial → nuvem (AWS / GCP / Azure)

---

## 🛠 Como Rodar / Instalar

```bash
# Exemplo de backend local
git clone https://github.com/KaduSR/AppIxc-central-do-assinante
cd fiberapp/backend
npm install
cp .env.example .env  # configurar TOKEN_IXC e URL_IXC
npm run dev
```

No chatbot (Node.js):
```bash
cd chatbot
npm install
node index.js
```

App Flutter Android:
```bash
cd mobile
flutter pub get
flutter run --release
```

---

## 🌐 API IXC – Integração

- Base URL: `https://seudominio/webservice/v1/`  
- Autenticação: header `Authorization: Bearer <TOKEN_IXC>`  
- Endpoints exemplo:  
  - `/cliente/boletos?cpf_cnpj=…`  
  - `/chamado` (POST)  

🔗 [Documentação oficial IXC](https://wikiapiprovedor.ixcsoft.com.br)  
🔗 [Coleção Postman IXC](https://documenter.getpostman.com/view/40255984/2sAYBbe9Ma)  

---

## 🤝 Contribuição & Feedback

Quer colaborar ou sugerir melhorias?  
1. Crie uma *issue* detalhando sua sugestão.  
2. Proponha um PR (pull request).  
3. Por favor, mantenha o padrão de código e adicione testes, se possível.  

Também apreciamos feedbacks sobre UX, fluxos e novas features.

---

## 📄 Licença

Este projeto está licenciado sob [MIT License](LICENSE).  
Você pode usar, modificar e distribuir, mas mantenha atribuição.

---

## 👥 Autores & Responsáveis

- **Kadu Ribeiro** (Product Owner / idealizador)  
- **Equipe de Desenvolvimento (futuro)**  
- **Suporte / Atendimento**  

---
