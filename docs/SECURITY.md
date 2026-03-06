# Security Policy

> Esta é a versão usada no trabalho do semestre. Não há suporte para versões anteriores.

---

| Ferramenta | Tipo | O que verifica | Quando executa |
| ----- | ----- | ----- | ----- |
| SonarQube | SAST/SCA | Qualidade e Segurança de código geral e dependências desatualizas | Scan Automático em Cloud |
| Qodana | SAST/SCA | Vulnerabilidades no código fonte Kotlin e dependências desatualizadas | Scan Automático em Cloud |
| Semgrep | SAST | Vulnerabilidades no código fonte | CI - A cada Push/PR |
| Trivy | Container Scan | CVEs em Imagens Docker e dependências | CI - A cada Push/PR |
| Nuclei | DAST | Scan baseado em template por envio de requisições para identificar vulnerabilidades | CI - A cada Push/PR |

---

## Reporting a Vulnerability

Se você encontrar uma vulnerabilidade neste projeto, **não abra uma issue pública**.

Entre em contato pelo e-mail: **joaomarcos.aquino@hotmail.com**

---

## CVE Tracking

Vulnerabilidades identificadas via Trivy e acompanhadas pela equipe de segurança.

| CVE | Pacote | Severidade | Status | Decisão | Revisão |
| --- | --- | --- | --- | --- | --- |
| CVE-2023-45853 | zlib | CRITICAL | Sem fix (Debian `<ignored>`) | Risco aceito. MiniZip não compilado no Debian; zlib `1.3.1-r2` no runtime já corrigido | 04/03/2026 |
| CVE-2025-7458 | libsqlite3-0 | CRITICAL | Sem fix (Debian `<no-dsa>`) | Risco aceito. Presente apenas no build stage, não copiado para runtime | 04/03/2026 |
| CVE-2026-25646 | libpng | HIGH | :white_check_mark: Corrigido em `1.6.55-r0` | Corrigido na imagem atual | 04/03/2026 |
| CVE-2026-1584 | - | - | RESERVED - não publicada | Monitorando - sem detalhes disponíveis | 04/03/2026 |
| CVE-2023-2953 | libldap | HIGH | Sem fix (Debian `<no-dsa>`) | Risco aceito. Sem uso de LDAP na aplicação | 04/03/2026 |
| CVE-2026-0861 | libc6 | HIGH | Sem fix (Debian `<no-dsa>`) | Risco aceito. Condições restritas | 04/03/2026 |
| CVE-2026-0861 | libc-bin | HIGH | Sem fix (Debian `<no-dsa>`) | Risco aceito. Condições restritas | 04/03/2026 |
| GHSA-72hv-8253-57qq | tools.jackson.core:jackson-core | HIGH | Corrigido em `3.1.0` | Versão corrigida fixada em arquivo de Dependências | 04/03/2026 |


---
