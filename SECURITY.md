# Security Policy

## Supported Versions

| Version | Supported          |
| ------- | ------------------ |
| 1.0     | :white_check_mark: |
| < 1.0   | :x:                |

> Esta é a versão usada no semestre. Não há suporte para versões anteriores.

---

## Reporting a Vulnerability

Se você encontrar uma vulnerabilidade neste projeto, **não abra uma issue pública**.

Entre em contato pelo e-mail: **joaomarcos.aquino@hotmail.com**  

---

## CVE Tracking

Vulnerabilidades identificadas via Trivy e acompanhadas pela equipe de segurança.

| CVE | Pacote | Severidade | Status | Decisão | Revisão |
| --- | --- | --- | --- | --- | --- |
| CVE-2023-45853 | zlib | CRITICAL | Sem fix (Debian `<ignored>`) | Risco aceito — MiniZip não compilado no Debian; zlib `1.3.1-r2` no runtime já corrigido | 04/03/2026 |
| CVE-2025-7458 | libsqlite3-0 | CRITICAL | Sem fix (Debian `<no-dsa>`) | Risco aceito - presente apenas no build stage, não copiado para runtime | 04/03/2026 |
| CVE-2026-25646 | libpng | HIGH | ✅ Corrigido em `1.6.55-r0` | Corrigido na imagem atual | 04/03/2026 |
| CVE-2026-1584 | - | - | RESERVED - não publicada | Monitorando - sem detalhes disponíveis | 04/03/2026 |

---

## Security Tools

| Ferramenta | Uso |
| --- | --- |
| Trivy | Scan de vulnerabilidades em imagens Docker e filesystem |
| Semgrep | SAST, SCA e Secret Management |
| Sonarqube | Análise Estática de Qualidade e Segurança |

---

## Review Policy

- CVEs com status **RESERVED** são revisadas mensalmente
- CVEs aceitas são reavaliadas a cada nova versão do projeto
