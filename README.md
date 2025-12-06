# Política de Privacidade

## AFB - Sistema de Controle de Acesso

**Última atualização:** {{06/12/2025}}

---

## 1. Introdução

Esta Política de Privacidade descreve como o **AFB - Sistema de Controle de Acesso** ("nós", "nosso" ou "sistema") coleta, usa, armazena e protege suas informações pessoais, incluindo dados biométricos faciais.

Ao utilizar nosso sistema, você concorda com as práticas descritas nesta política.

---

## 2. Dados Coletados

### 2.1 Dados Biométricos

- **Fotos faciais**: Imagens capturadas para reconhecimento facial
- **Embeddings faciais**: Representações matemáticas do rosto (128 dimensões) geradas pelo modelo MobileFaceNet
- **Descritores faciais**: Dados técnicos extraídos das imagens para identificação

### 2.2 Dados Pessoais

- **Nome completo**
- **CPF** (quando fornecido)
- **Empresa/Organização** (quando aplicável)
- **E-mail** (para usuários administrativos via Google OAuth)

### 2.3 Dados de Acesso e Controle

- **Horários de entrada e saída**
- **Data e hora dos registros de acesso**
- **Status de acesso** (Autorizado, Bloqueado, Pendente)
- **Motivos de bloqueio** (quando aplicável)
- **Informações de veículos** (placa, marca) - quando fornecidas

### 2.4 Dados Técnicos

- **Device ID** (identificador único do dispositivo Android)
- **Informações de licença do sistema**
- **Logs de sistema** (para auditoria e troubleshooting)

### 2.5 Dados de Autenticação

- **Credenciais do Google OAuth** (para usuários administrativos)
- **Role/Papel do usuário** (admin, operacional)
- **Sessões de autenticação**

---

## 3. Finalidades do Tratamento

Os dados coletados são utilizados exclusivamente para:

### 3.1 Controle de Acesso

- Identificação de pessoas através de reconhecimento facial
- Verificação de autorização de entrada
- Registro de entrada e saída
- Prevenção de acesso não autorizado

### 3.2 Segurança

- Verificação contra listas de bloqueio (blocklist)
- Auditoria de acessos
- Registro de eventos de segurança
- Prevenção de fraudes

### 3.3 Gestão do Sistema

- Cadastro e gerenciamento de pessoas autorizadas
- Agendamento de visitas
- Gerenciamento de usuários administrativos
- Geração de relatórios de acesso

### 3.4 Melhoria do Serviço

- Análise de padrões de acesso (anônimos e agregados)
- Otimização do sistema de reconhecimento
- Correção de erros e melhorias técnicas

---

## 4. Base Legal

O tratamento de dados pessoais e biométricos é realizado com base em:

- **Consentimento**: Quando você fornece seus dados voluntariamente
- **Execução de contrato**: Para cumprimento de obrigações contratuais de controle de acesso
- **Legítimo interesse**: Para segurança patrimonial e prevenção de fraudes
- **Cumprimento de obrigação legal**: Quando exigido por lei ou ordem judicial

**Nota sobre dados biométricos**: O tratamento de dados biométricos é realizado exclusivamente para fins de controle de acesso e segurança, conforme previsto na Lei Geral de Proteção de Dados (LGPD - Lei 13.709/2018).

---

## 5. Armazenamento e Segurança

### 5.1 Localização dos Dados

- **Banco de dados**: Supabase (PostgreSQL) - servidores localizados conforme política do Supabase
- **Fotos faciais**: Supabase Storage (bucket `face-photos`)
- **Processamento local**: Reconhecimento facial processado no dispositivo Android (não enviado para servidores externos durante o processamento)

### 5.2 Medidas de Segurança

Implementamos medidas técnicas e organizacionais para proteger seus dados:

- **Criptografia**: Dados transmitidos via HTTPS/TLS
- **Autenticação**: Sistema de autenticação OAuth 2.0
- **Controle de acesso**: Row Level Security (RLS) no banco de dados
- **Isolamento**: Dados biométricos armazenados separadamente
- **Auditoria**: Logs de acesso e modificação de dados
- **Backup seguro**: Backups criptografados e protegidos

### 5.3 Processamento Local

O reconhecimento facial é processado **localmente no dispositivo Android** usando:
- **ML Kit** (Google) para detecção de rostos
- **MobileFaceNet** (TensorFlow Lite) para geração de embeddings

Os embeddings são gerados no dispositivo e apenas o resultado (não a imagem original) é comparado com o banco de dados.

---

## 6. Compartilhamento de Dados

### 6.1 Não Compartilhamos Dados com Terceiros

**Não vendemos, alugamos ou compartilhamos seus dados pessoais ou biométricos com terceiros**, exceto nas seguintes situações:

### 6.2 Exceções Legais

- **Ordem judicial**: Quando exigido por lei ou ordem judicial
- **Autoridades competentes**: Quando solicitado por autoridades policiais ou judiciárias
- **Prestadores de serviço**: Apenas prestadores de serviço técnico (Supabase) que atuam como processadores de dados, sob contrato de confidencialidade

### 6.3 Acesso Interno

Apenas os seguintes perfis têm acesso aos dados:

- **Administradores do sistema**: Acesso completo para gestão
- **Usuários operacionais**: Acesso limitado para operação do sistema
- **Equipe técnica**: Acesso técnico para manutenção e suporte

---

## 7. Retenção de Dados

### 7.1 Período de Retenção

- **Dados biométricos e fotos**: Mantidos enquanto a pessoa estiver cadastrada no sistema e por até **2 (dois) anos** após remoção do cadastro, para fins de auditoria e segurança
- **Registros de acesso**: Mantidos por **5 (cinco) anos** para fins de auditoria e cumprimento legal
- **Dados de usuários administrativos**: Mantidos enquanto a conta estiver ativa e por até **1 (um) ano** após desativação

### 7.2 Exclusão de Dados

Você pode solicitar a exclusão de seus dados a qualquer momento, exceto quando:

- A retenção for necessária para cumprimento de obrigação legal
- Os dados forem necessários para exercício regular de direitos
- Os dados forem necessários para proteção de direitos de terceiros

---

## 8. Seus Direitos (LGPD)

Conforme a Lei Geral de Proteção de Dados (LGPD), você tem os seguintes direitos:

### 8.1 Direitos Garantidos

- **Confirmação e acesso**: Saber se tratamos seus dados e acessá-los
- **Correção**: Solicitar correção de dados incompletos, inexatos ou desatualizados
- **Anonimização, bloqueio ou eliminação**: Solicitar remoção de dados desnecessários ou excessivos
- **Portabilidade**: Solicitar portabilidade dos dados para outro fornecedor
- **Eliminação**: Solicitar exclusão de dados tratados com consentimento
- **Informação**: Obter informações sobre compartilhamento de dados
- **Revogação de consentimento**: Revogar consentimento a qualquer momento
- **Revisão de decisões automatizadas**: Solicitar revisão de decisões tomadas exclusivamente por processamento automatizado

### 8.2 Como Exercer Seus Direitos

Para exercer seus direitos, entre em contato conosco através dos canais indicados na seção [Contato](#12-contato).

---

## 9. Cookies e Tecnologias Similares

Este sistema utiliza:

- **Cookies de sessão**: Para manter sua autenticação
- **Local Storage**: Para armazenamento local de preferências
- **Não utilizamos cookies de rastreamento ou publicidade**

---

## 10. Menores de Idade

Este sistema não coleta intencionalmente dados de menores de 18 anos sem consentimento dos responsáveis legais. Se você é responsável por um menor e acredita que seus dados foram coletados, entre em contato conosco imediatamente.

---

## 11. Alterações nesta Política

Podemos atualizar esta Política de Privacidade periodicamente. Quando houver alterações significativas:

- **Notificaremos** através do sistema ou por e-mail
- **Atualizaremos** a data de "Última atualização" no topo desta página
- **Solicitaremos novo consentimento** quando necessário

Recomendamos revisar esta política periodicamente.

---

## 12. Contato

Para questões sobre privacidade, proteção de dados ou para exercer seus direitos, entre em contato:

### 12.1 Encarregado de Proteção de Dados (DPO)

**Nome**: [SEGMA LABS]  
**E-mail**: [isfiasegurancanotrabalho@gmail.com]  

### 12.2 Suporte Técnico

**E-mail**: [isfiasegurancanotrabalho@gmail.com]  

### 12.3 Endereço

[ENDEREÇO_COMPLETO]

---

## 13. Legislação Aplicável

Esta Política de Privacidade é regida pela **Lei Geral de Proteção de Dados (LGPD - Lei 13.709/2018)** e demais legislações brasileiras aplicáveis.

---

## 14. Consentimento

Ao utilizar o sistema AFB - Controle de Acesso, você declara ter lido, compreendido e concordado com esta Política de Privacidade.

**Data de consentimento**: Será registrada no momento do primeiro uso do sistema.

---

## Anexos

### Anexo A - Glossário

- **Embedding facial**: Representação matemática do rosto em forma de vetor numérico (128 dimensões)
- **MobileFaceNet**: Modelo de reconhecimento facial baseado em deep learning
- **ML Kit**: Biblioteca do Google para machine learning em dispositivos móveis
- **RLS (Row Level Security)**: Política de segurança no nível de linha do banco de dados
- **Supabase**: Plataforma de backend como serviço (BaaS)

### Anexo B - Informações Técnicas

- **Modelo de reconhecimento**: MobileFaceNet (TensorFlow Lite)
- **Dimensões do embedding**: 128 valores numéricos
- **Threshold de similaridade**: 0.6 (60%)
- **Plataforma**: Android nativo (obrigatório para reconhecimento facial)

---

**Versão**: 1.0  
**Data**: {{06/12/2025}}
**Status**: Ativa

