# Vittoria

**Agendamento conversacional para negócios de serviços: marcar, remarcar e cancelar atendimentos por chat, com transferência para atendente humano e controle de acesso integrados.**

> **Apenas vitrine.** Este repositório apresenta o produto Vittoria a potenciais parceiros e clientes. **Não contém código-fonte** e **não concede licença** de qualquer tipo. Veja o [Aviso](#aviso).

English: [README.md](README.md)

---

## O que é a Vittoria

A Vittoria é um assistente multiempresa (multi-tenant) que permite aos clientes de um negócio de serviços gerenciar seus agendamentos em uma conversa. Cada empresa mantém sua própria agenda, regras e usuários; o assistente cuida do diálogo repetitivo de agendamento e passa a conversa a uma pessoa quando necessário.

## Estágio de desenvolvimento

A Vittoria está **em desenvolvimento ativo**. As capacidades abaixo foram exercitadas em **ambiente de desenvolvimento, com dados fictícios e testes automatizados**. **Não** são apresentadas como certificadas, auditadas ou comprovadas em produção, e esta página não faz afirmação sobre uso em produção.

| Capacidade | Estágio |
|---|---|
| Agendamento, remarcação e cancelamento por conversa | Funcionando em desenvolvimento; testado com dados sintéticos |
| Transferência para atendimento humano | Funcionando em desenvolvimento; testado com dados sintéticos |
| Operação multiempresa (dados separados por negócio; isolamento testado) | Funcionando em desenvolvimento; testado com dados sintéticos |
| Controle de acesso para administradores e operadores | Funcionando em desenvolvimento; testado com dados sintéticos |
| Backups criptografados e verificados dos bancos de dados do negócio | Funcionando em desenvolvimento; testado com dados sintéticos (agendamento automático dos backups ainda pendente) |
| Registros (logs) do tratamento de mensagens limitados a categorias fixas (sem texto de mensagens, telefones ou identificadores) | Funcionando em desenvolvimento; coberto por testes automatizados |
| Recebimento de mensagens com assinatura, limite de tamanho e de frequência | Funcionando em desenvolvimento |
| Fuso horário por negócio (incluindo casos de horário de verão) | Testado com dados sintéticos; um fuso usado em testes iniciais |
| Português (Brasil) como idioma de referência | Funcionando em desenvolvimento |
| Inglês e espanhol | **Experimental** — aguardam revisão por falantes nativos |
| Entrega pelo WhatsApp via API oficial Meta Business Cloud | **Em validação** — não anunciada como operacional |
| Painéis, cobrança, canais adicionais | **Planejados** — indisponíveis |

## Arquitetura conceitual

```
 Canal de conversa do cliente
          |
          v
   Entrada segura de mensagens  (autenticação, validação, limites)
          |
          v
   Motor de diálogo  <---->  Camada de idiomas (catálogos, formatação)
          |
          v
   Serviço de agenda  <---->  Armazenamento por negócio (backups criptografados)
          |
          v
   Atendimento humano / administração (com controle de acesso)
```

Cada negócio ("tenant") tem dados e configurações isolados. Detalhes de implementação não são publicados de propósito.

## Oportunidades comerciais

Temos interesse em conversar com empresas sobre:

- **Demonstrações** com dados fictícios.
- **Parcerias** (implantação, integração, indicação).
- **Licenciamento, serviço gerenciado, implantação e suporte**.

Tudo o que precede está **sujeito a formalização contratual**. Nada neste repositório é oferta, tabela de preços ou contrato.

## Contato

Contato comercial: a divulgar.

## Aviso

- Este repositório é uma **vitrine**. Não disponibiliza código-fonte, binários, instaladores nem documentação suficiente para executar o produto.
- **Nenhuma licença** é concedida — nem licença de código aberto, nem direito de usar, copiar, modificar ou distribuir qualquer software do produto, nem direitos de marca. Todos os direitos são reservados a seus respectivos titulares.
- As descrições refletem o estado de desenvolvimento na data da publicação e podem mudar sem aviso. Os estágios acima não são garantias nem compromissos.
- Nomes e marcas citados (por exemplo WhatsApp e Meta) pertencem a seus donos; não se declara afiliação, endosso nem parceria oficial.
