💸 Consórcio Entre Amigos
Sistema colaborativo para organização de consórcios informais entre amigos, com sorteios mensais e controle de pagamentos via comprovante de PIX.

📌 Funcionalidades Principais
Registro e login de usuários (com recuperação de senha)

Criação de consórcios personalizados

Link de convite para novos participantes

Período de inscrições controlado

Sorteios automáticos mensais

Visualização da chave PIX do contemplado

Upload e validação de comprovantes de pagamento

Painel com status dos participantes

🛠️ Tecnologias
Next.js — React Framework

ShadCN UI — Componentes estilizados com TailwindCSS

Prisma — ORM para banco de dados

PostgreSQL — Banco de dados relacional

NextAuth.js — Autenticação segura

Zod — Validação de formulários e schemas

Docker (com banco de dados dentro) 

🚀 Como Funciona o Sistema
1. Cadastro e Login
Campos: nome, e-mail, senha, chave PIX.

Login seguro com autenticação de sessão.

Recuperação de senha via e-mail.

2. Criação de Consórcio
Qualquer usuário logado pode criar um novo consórcio.

Define:

Nome do consórcio

Valor mensal

Período de inscrição

Após criar, recebe um link exclusivo para compartilhar com amigos.

3. Participação
Apenas usuários logados podem entrar em consórcios.

Criador pode adicionar manualmente usuários já cadastrados ou remover integrantes.

4. Encerramento das Inscrições
O criador define:

Data inicial do sorteio

Dia fixo dos pagamentos mensais

5. Sorteios e Pagamentos
Sorteio mensal automático na data definida.

O sorteado do mês terá sua chave PIX exibida no painel.

Cada participante envia o valor por PIX diretamente ao contemplado.

6. Confirmação de Pagamento
Participante faz upload do comprovante via dashboard.

O sorteado pode:

Validar: o sistema atualiza o último mês pago do usuário.

Recusar: o sistema solicita novo comprovante.

🖥️ Dashboard
Cards de Consórcios
Visualização rápida dos consórcios ativos, encerrados e pendentes.

Tela do Consórcio (exemplo)
Nome do consórcio

Valor mensal

Participantes:

Indicador se já foi sorteado

Último mês pago

PIX do sorteado do mês

Seção de upload de comprovante

🔒 Segurança
Autenticação com NextAuth.js

Validação de uploads e permissões de visualização

Dados de PIX visíveis apenas aos participantes

📅 Roadmap Futuro
 Sistema de notificações por e-mail

 Histórico completo de pagamentos

 Exportação em PDF dos dados

 API pública para integrações externas

👨‍💻 Contribuição
Fork este repositório

Crie sua feature branch: ---

Commit suas alterações: ----

Push para o branch remoto: ---

Crie um Pull Request

📃 Licença
MIT © 2025 — repingo.club
