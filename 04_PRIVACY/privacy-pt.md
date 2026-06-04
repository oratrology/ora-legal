# POLÍTICA DE PRIVACIDADE — ORA Plataforma de IA Esotérica
## Versão 2.3 | 4 de junho de 2026
## Controlador de dados: Santiago Sáiz / Fundación Hostelling del Ecuador
## privacy@oratrology.com | dpo@oratrology.com

---

## PRINCÍPIOS-CHAVE
- Coletamos apenas o necessário
- Nunca vendemos seus dados
- Dados biométricos excluídos imediatamente após a leitura
- Dados de análise emocional nunca armazenados — apenas em tempo real
- Dados de localização (cidade de nascimento) transmitidos ao Google apenas durante o autocompletar do onboarding
- Componentes open source apenas para cálculos — seus dados nunca processados por eles de forma identificável

---

## 1. DADOS COLETADOS

- Identidade: nome, e-mail
- Dados de nascimento: data, hora, local
- **Dados de localização:** cidade ou local de nascimento inserido durante o onboarding (ver Seção 6 — API Google Places)
- Visuais: fotos de mão, íris, café
- Narrativos: descrições de sonhos, perguntas pessoais
- Pagamento: processado por Apple/Google/Stripe/PayPal (não armazenado pela ORA)
- Coletados automaticamente: info do dispositivo, uso, IP, localização geral, análises (anonimizadas)

Dados biométricos (mão/íris): consentimento duplo, exclusão imediata após leitura, criptografia TLS 1.3 + AES-256, nunca compartilhados exceto com Anthropic Claude API sob DPA.

Análise emocional passiva: apenas em tempo real, sem gravação, nunca transmitida a terceiros.

---

## 2. COMPONENTES OPEN SOURCE

ORA usa componentes open source (Swiss Ephemeris sob AGPLv3) exclusivamente para cálculos astronômicos. Seus dados pessoais NUNCA são processados por esses componentes de forma identificável.

---

## 3. BASE LEGAL (GDPR/LGPD)

| Atividade | Base |
|-----------|------|
| Conta/leituras/pagamentos | Contrato |
| Dados biométricos | Consentimento explícito |
| Dados de nascimento | Consentimento explícito |
| Análise emocional | Consentimento explícito + Interesse legítimo |
| Autocompletar localização (onboarding) | Interesse legítimo |
| Análises | Interesse legítimo |
| Marketing | Consentimento |

---

## 4. RETENÇÃO DE DADOS

| Dado | Período |
|------|---------|
| Dados de conta | Duração da conta + 3 anos |
| Histórico de leituras | Conta + 1 ano |
| Fotos biométricas | EXCLUSÃO IMEDIATA após leitura |
| Dados de análise emocional | NÃO RETIDOS — apenas sessão em tempo real |
| Outras fotos (café) | 90 dias após leitura |
| Cidade de nascimento | Duração da conta |
| Registros de pagamento | 7 anos (lei fiscal do Equador) |
| Análises (anon) | 3 anos |

---

## 5. COMPARTILHAMENTO DE DADOS

| Provedor | Função | Dados compartilhados | Localização |
|----------|--------|----------------------|-------------|
| Supabase | BD / auth / armazenamento | Conta + dados de leituras | EUA (AWS) |
| Anthropic Claude | Geração de leituras IA | Dados de nascimento, contexto | EUA |
| Apple (App Store / IAP) | Distribuição app, pagamentos | Apenas tokens de compra | EUA |
| Google (Firebase / Auth) | Autenticação, notificações push | Token de dispositivo, credenciais auth | EUA |
| **Google (API Places)** | **Autocompletar local de nascimento — apenas onboarding** | **Texto parcial do local digitado pelo usuário** | **EUA** |
| Stripe / PayPal | Pagamentos | Dados de pagamento tokenizados | EUA |
| OneSignal | Notificações push | Token de dispositivo | EUA |

**Transferências UE:** Cláusulas Contratuais Padrão (SCCs).
**Sem venda de dados. Sem atividade de corretor de dados.**

### 5.1 API Google Places — Divulgação Específica

ORA integra a API Google Places Autocomplete exclusivamente durante o onboarding para ajudar o usuário a inserir sua cidade de nascimento:

- **O que é enviado ao Google:** apenas o texto parcial digitado no campo de local de nascimento
- **O que o Google NÃO recebe:** nome, e-mail, data/hora de nascimento, fotos, leituras ou outros dados pessoais
- **O que a ORA armazena:** apenas o nome do local selecionado, no perfil para cálculos astrológicos
- **Processamento pelo Google:** regido pelos Termos de Serviço do Google (https://developers.google.com/maps/terms) e pela Política de Privacidade do Google (https://policies.google.com/privacy)
- **Alternativa:** você pode digitar sua cidade manualmente — o autocompletar não é obrigatório

A ORA não é responsável pelas práticas de tratamento de dados do Google além desta divulgação.

---

## 6. SEUS DIREITOS

Acesso, Correção, Exclusão, Portabilidade, Revogação do Consentimento, Reclamação à ANPD (gov.br/anpd).
Contato: privacy@oratrology.com — Resposta: 30 dias.

---

## 7. CONTATO

privacy@oratrology.com | dpo@oratrology.com | legal@oratrology.com
Hub Legal: https://oratrology.com/legal/

---

## CHANGELOG

| Versão | Data | Alterações |
|--------|------|------------|
| v2.3 | 4 jun 2026 | Seção 1: "Dados de localização" adicionados. Seção 3: base legal para autocompletar. Seção 5: Google separado em duas entradas (Firebase/Auth e API Places). Seção 5.1 adicionada: divulgação específica API Google Places. |
| v2.2 | 3 jun 2026 | Seção 2 adicionada: componentes open source AGPLv3. |
| v2.1 | 14 mai 2026 | Dados biométricos e análise emocional adicionados. |
| v2.0 | 11 mai 2026 | Versão inicial publicada. |

*ORA Política de Privacidade v2.3 | Santiago Sáiz / Fundación Hostelling del Ecuador | oratrology.com*
