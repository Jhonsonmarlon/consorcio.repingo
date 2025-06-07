# 💸 Consórcio Entre Amigos

Sistema colaborativo para organização de consórcios informais entre amigos, com sorteios mensais e controle de pagamentos via comprovante de PIX.

## 📌 Funcionalidades Principais
- Registro e login de usuários (com recuperação de senha)
- Criação de consórcios personalizados
- Link de convite para novos participantes
- Período de inscrições controlado
- Sorteios automáticos mensais
- Visualização da chave PIX do contemplado
- Upload e validação de comprovantes de pagamento
- Painel com status dos participantes

## 🛠️ Tecnologias
- Next.js — React Framework
- ShadCN UI — Componentes estilizados com TailwindCSS
- Prisma — ORM para banco de dados
- PostgreSQL — Banco de dados relacional
- NextAuth.js — Autenticação segura
- Zod — Validação de formulários e schemas
- Docker (com banco de dados dentro)

## Instalação
1. Instale as dependências:
   ```bash
   npm install
   # ou
   yarn
   ```
2. Configure as variáveis de ambiente copiando `.env.example` para `.env` e ajustando:
   ```env
   DATABASE_URL=postgresql://usuario:senha@localhost:5432/consorcio
   NEXTAUTH_URL=http://localhost:3000
   NEXTAUTH_SECRET=sua_chave_secreta
   ```
3. Inicie os serviços de apoio (banco de dados) com Docker:
   ```bash
   docker compose up -d
   ```
4. Execute as migrações do banco de dados:
   ```bash
   npx prisma migrate dev
   ```
5. Rode o servidor de desenvolvimento:
   ```bash
   npm run dev
   # ou
   yarn dev
   ```

## 🚀 Como Funciona o Sistema
1. **Cadastro e Login**
   - Campos: nome, e-mail, senha, chave PIX.
   - Login seguro com autenticação de sessão.
   - Recuperação de senha via e-mail.
2. **Criação de Consórcio**
   - Qualquer usuário logado pode criar um novo consórcio.
   - Define nome do consórcio, valor mensal e período de inscrição.
   - Após criar, recebe um link exclusivo para compartilhar com amigos.
3. **Participação**
   - Apenas usuários logados podem entrar em consórcios.
   - Criador pode adicionar manualmente usuários já cadastrados ou remover integrantes.
4. **Encerramento das Inscrições**
   - O criador define a data inicial do sorteio e o dia fixo dos pagamentos mensais.
5. **Sorteios e Pagamentos**
   - Sorteio mensal automático na data definida.
   - O sorteado do mês terá sua chave PIX exibida no painel.
   - Cada participante envia o valor por PIX diretamente ao contemplado.
6. **Confirmação de Pagamento**
   - Participante faz upload do comprovante via dashboard.
   - O sorteado pode validar (atualizando o último mês pago) ou recusar o comprovante.

## 🖥️ Dashboard
- Cards de consórcios para visualização rápida dos ativos, encerrados e pendentes.
- Tela do consórcio com:
  - Nome do consórcio
  - Valor mensal
  - Participantes
  - Indicador se já foi sorteado
  - Último mês pago
  - PIX do sorteado do mês
  - Seção de upload de comprovante

## 🔒 Segurança
- Autenticação com NextAuth.js
- Validação de uploads e permissões de visualização
- Dados de PIX visíveis apenas aos participantes

## 📅 Roadmap Futuro
- Sistema de notificações por e-mail
- Histórico completo de pagamentos
- Exportação em PDF dos dados
- API pública para integrações externas

## 👨‍💻 Contribuição
1. Fork este repositório.
2. Crie sua branch de feature:
   ```bash
   git checkout -b minha-feature
   ```
3. Commit suas alterações:
   ```bash
   git commit -m "feat: minha feature"
   ```
4. Envie para o repositório remoto:
   ```bash
   git push origin minha-feature
   ```
5. Abra um Pull Request.

## 📃 Licença
MIT © 2025 — repingo.club
