<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/assinatura-horizontal-escuro.png">
  <img src="assets/assinatura-horizontal-claro.png" alt="MemorySmith.app" width="672">
</picture>

<br>

**Structured knowledge, natively readable and writable by agents.**

*Cada nota vira um nó. Cada leitura cria uma aresta.*

</div>

---

## O que é

O **MemorySmith.app** é a plataforma de **cofres de conhecimento em Markdown, com estrutura declarada, acessíveis nativamente pelas ferramentas de IA** através de MCP.

O fluxo que já funciona hoje é uma pasta local de arquivos `.md`, com um documento na raiz explicando ao agente como estruturar as notas. O MemorySmith.app é o backend remoto desse fluxo: mantém o formato (Markdown puro), mantém a prática (orientação na raiz, modelo por pasta) e acrescenta o que a pasta local não tem — acesso remoto autenticado, colaboração com papéis, histórico defensável e descoberta por grafo e por significado.

## Como um vault se organiza

```
Vault
├── Guidance           ← para que serve este vault e como estruturar as notas
└── Pastas (ordenadas) ← cada uma com uma descrição: o que se guarda aqui
    ├── Template       ← como as notas desta pasta se estruturam
    ├── subpastas (ordenadas)
    └── notas .md
```

Guidance e Template não são documentação: são **instruções executáveis**. São o que faz o agente escrever a nota certa, na pasta certa, no formato certo.

## O ciclo de uso

O agente não só lê o vault — ele o **alimenta**:

1. **Ingestão.** O agente lê um corpo de material (normas, legislação, documentação, pesquisa) e o estrutura como notas, obedecendo às orientações do próprio vault.
2. **Consumo.** Depois, outro trabalho — uma auditoria, um relatório, um parecer — usa o mesmo vault como base de conhecimento estruturada.

## Pilares

| | |
|---|---|
| 🔌 **MCP como contrato público** | Conector nativo para plataformas de IA (OAuth 2.1). `get_vault_context` devolve a orientação integral mais a árvore anotada em uma única chamada |
| ✍️ **Autoria completa** | Toda escrita registra o humano dono da autorização **e** o agente que executou. Não existe alteração anônima |
| 🕸️ **Descoberta** | Grafo de links, backlinks e busca semântica — sempre derivados dos `.md`, nunca fonte da verdade |
| 📜 **O passado é imutável** | Histórico por revisão e trilha append-only. A base pode ser lida como ela estava na data de emissão de um trabalho |
| 📦 **Zero lock-in** | Export devolve `.md` puros numa árvore de arquivos legível, sem formato proprietário |

---

<div align="center">
  <sub>© MemorySmith.app · Em construção 🚧</sub>
</div>
