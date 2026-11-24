# Regis Rodrigo Dobre

**Engenheiro de Software Full-Stack & Arquiteto de Sistemas**  
PHP / Laravel · JavaScript · Python · IA Aplicada · Infraestrutura Linux & Segurança

Construo, integro e opero **sistemas críticos em produção ponta a ponta** — da modelagem de banco e backend à interface responsiva, hardening de servidores Linux e entrega contínua. Sou fundador da [Dobre Tecnologia](https://dobretecnologia.com), onde arquiteto plataformas web, soluções GovTech e automações com IA generativa.

> **Sobre os repositórios privados:** A maioria dos sistemas que desenvolvo e mantenho opera sob contratos ativos de produção (setor público e privado), razão pela qual seus repositórios permanecem privados por confidencialidade e segurança. Abaixo está um panorama técnico da minha stack, das arquiteturas em produção e do pacote open-source disponível neste perfil.

---

## Sistemas & Arquiteturas em Produção

### 1. Ecossistema GovTech Municipal *(Produção 24/7)*
* **Diário Oficial Eletrônico (`Laravel · PHP 8.3 · MySQL · ICP-Brasil`):**
  * Motor automatizado de diagramação, fila de publicação com consolidação atômica e rollback de segurança.
  * Conversão fiel de documentos `.docx`/`.doc` para PDF via **LibreOffice Headless** e extração de texto em C++ com **Poppler (`pdftotext`)**, reduzindo consumo de RAM em lotes de dezenas de PDFs de >1 GB para ~22 MB.
  * Pipeline de **OCR Sandwich** pesquisável (`ocrmypdf` + Tesseract) controlado por **mutex global (`flock`)**, prioridade reduzida (`nice`) e cache em disco para evitar picos de concorrência.
  * **Assinatura digital criptográfica ICP-Brasil (PAdES / PKCS#7 / SHA-256)** com certificados A1 validada pelo Verificador do ITI e Adobe Reader, além de mascaramento de CPF (LGPD).
* **Infraestrutura de Correio Corporativo & Webmail Customizado (`Postfix · Dovecot · SnappyMail · JS/CSS · Gemini API`):**
  * Servidor de e-mail dedicado com autenticação **SPF / DKIM / DMARC**, canais cifrados **TLSv1.3 (IMAPS/POP3S)** e suporte a anexos de até **1 GB**.
  * Camada de interface moderna (modos Claro/Escuro, `<dialog>` nativo, pré-visualização segura inline de PDFs, XMLs de NF-e e imagens antes do envio/encaminhamento) e assistente de IA isolado com controle de cota por caixa.
* **Portais Institucionais, Ouvidoria / e-SIC & Auditoria Unificada (`WordPress · Laravel`):**
  * Temas e plugins sob medida em arquitetura **SOLID / PSR-4**, Portal da LGPD, conformidade **ATRICON / PNTP** e **LAI (Ouvidoria & e-SIC)**.
  * Central unificada de auditoria integrando eventos do Diário Oficial, SMTP e WordPress com captura de IP real atrás de proxy reverso (`CF-Connecting-IP`).

### 2. IA Aplicada & Automação
* **Assistentes com LLMs (`Node.js · Python · Google Gemini API`):**
  * Orquestração de atendimento automatizado (Web, voz/TTS e WhatsApp) com **Structured Outputs (JSON Schema)** e isolamento de chaves/cotas por projeto.
  * Integrações com APIs públicas, incluindo monitoramento de contratações no **PNCP (Portal Nacional de Contratações Públicas)**.

### 3. Plataformas Web & Gestão
* **Sistema Legislativo:** plataforma de gestão parlamentar (leis, indicações, sessões e trilha pública auditável para Câmaras Municipais).
* **VerifiCar:** sistema de gestão de frotas, proprietários, agências e vistorias com filtros universais e proteção de dados sensíveis (LGPD).
* **Conecta Fronteira:** portal de notícias multi-editorial desenvolvido em **Laravel + Filament** com automação de publicação.

### 4. Infraestrutura, Segurança & Alta Disponibilidade
* **Hardening & Perímetro:** Ubuntu LTS, Nginx, PHP-FPM, MariaDB, Redis, proteção de origem atrás de **Cloudflare WAF + IPTables (CIS Controls)**, mitigação de alertas **CTIR Gov**, headers de segurança nota **A+**.
* **Resiliência:** tuning de memória/Swap, proteção contra OOM-Killer (`OOMScoreAdjust`) e auto-recuperação via `systemd`, backups automatizados e esteiras de deploy via Git/SSH.

---

## Stack Principal

| Camada | Tecnologias |
| :--- | :--- |
| **Backend** | PHP 8.3, Laravel, Filament, WordPress (SOLID / PSR-4), Node.js, Python |
| **Frontend** | JavaScript (ES6+), HTML5, CSS3 moderno (Top-Layer `<dialog>`/`popover`, Acessibilidade, Design Systems) |
| **Dados & Mensageria** | MySQL, MariaDB, SQLite, Redis, Postfix, Dovecot, IMAP/SMTP |
| **Documentos, Cripto & IA** | ICP-Brasil (PAdES/X.509/OpenSSL), OCR (`ocrmypdf`/Tesseract), LibreOffice Headless, Poppler, Google Gemini API |
| **Infra & Segurança** | Linux (Ubuntu LTS), Nginx, PHP-FPM, Cloudflare WAF/DNS, IPTables, Systemd, Git/SSH |

---

## Open Source em Destaque

* **[`dobre-widgets`](https://github.com/regisciarama-code/dobre-widgets)** — Pacote Composer (licença MIT) de componentes Blade, interface Glassmorphism IHC e Autocomplete Universal para Laravel 9/10/11 (PHP 8.0–8.3).

---

## Contato

* **Site / Portfólio:** [dobretecnologia.com](https://dobretecnologia.com)
* **E-mail:** [contato@dobretecnologia.com](mailto:contato@dobretecnologia.com)
* **LinkedIn:** [linkedin.com/company/dobre-tecnologia-ltda](https://linkedin.com/company/dobre-tecnologia-ltda)
