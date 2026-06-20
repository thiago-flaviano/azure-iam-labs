# azure-iam-labs

Laboratórios práticos de Identity & Access Management no Microsoft Entra ID,
estruturados com base nos frameworks Zero Trust e CIS Benchmarks.

---

## Labs concluídos

### Lab 01 — Conditional Access: 3 políticas do zero

**Objetivo:** Implementar políticas de acesso condicional cobrindo os 
principais vetores de ataque em identidade corporativa.

**Políticas implementadas:**

| Política | Ação | Motivo |
|---|---|---|
| Block Legacy Authentication | Block access | Protocolos antigos não suportam MFA |
| Require MFA Outside Corporate IP | Require MFA | Acesso fora do perímetro exige segundo fator |
| Block Non-Operating Countries | Block access | Reduz superfície de ataque geográfica |

**Decisões técnicas:**
- Security Defaults desativado — pré-requisito para CA granular
- Break-glass account excluído de todas as políticas
- Named Location configurada com notação CIDR /32

**Evidências:**

> prints aqui — veja a seção abaixo

---

## Como usar

Todos os labs são executados em tenant de teste do Microsoft Entra ID.
Nenhum ambiente de produção foi utilizado.

## Referências

- [Microsoft SC-300 Study Guide](https://learn.microsoft.com/pt-br/credentials/certifications/resources/study-guides/sc-300)
- [CIS Microsoft 365 Benchmarks](https://www.cisecurity.org/benchmark/microsoft_365)
- [Zero Trust Architecture — NIST](https://www.nist.gov/publications/zero-trust-architecture)
