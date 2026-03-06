# Security

| Ferramenta | Tipo | O que verifica | Quando executa |
| ----- | ----- | ----- | ----- |
| SonarQube | SAST/SCA | Qualidade e Segurança de código geral e dependências desatualizas | Scan Automático em Cloud |
| Qodana | SAST/SCA | Vulnerabilidades no código fonte Kotlin e dependências desatualizadas | Scan Automático em Cloud |
| Semgrep | SAST | Vulnerabilidades no código fonte | CI - A cada Push/PR |
| Trivy | Container Scan | CVEs em Imagens Docker e dependências | CI - A cada Push/PR |
 | Nuclei | DAST | Scan baseado em template por envio de requisições para identificar vulnerabilidades | CI - A cada Push/PR |