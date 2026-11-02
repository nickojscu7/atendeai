# AtendeAI — MVP inicial

Aplicação Next.js + TypeScript + Supabase, com interface em português brasileiro e identidade azul royal, branco e dourado.

## O que este pacote contém
- Landing page.
- Cadastro e login via Supabase Auth.
- Painel protegido.
- Tela inicial de configuração do assistente.
- Telas-base de conversas e configurações.
- Esquema SQL inicial com empresas, membros, assistentes, clientes, conversas, mensagens, leads, conhecimento e assinaturas.
- RLS para isolamento por empresa.

## O que ainda NÃO está pronto
Este é o primeiro pacote de desenvolvimento, não um SaaS pronto para produção.
- O onboarding transacional que cria empresa e proprietário precisa ser concluído antes de liberar cadastros reais.
- Integração oficial do WhatsApp ainda não está implementada.
- Respostas de IA ainda não estão conectadas a um provedor.
- Cobranças recorrentes ainda não estão conectadas ao Mercado Pago/Stripe.
- Painel global do proprietário, relatórios avançados, automações e gestão de equipe ainda precisam ser construídos.
- O schema SQL deve ser revisado e testado em projeto Supabase antes de uso comercial.

## Requisitos
Node.js 20 ou superior.

## Rodar localmente
1. Instale dependências: `npm install`
2. Copie `.env.example` para `.env.local`.
3. Preencha URL e anon key do Supabase.
4. Execute `npm run dev`.
5. Abra `http://localhost:3000`.

## Publicação
É possível publicar pela Vercel conectando este projeto a um repositório GitHub. Configure as mesmas variáveis de ambiente no painel da Vercel.

## Segurança
- Nunca coloque chaves secretas em variáveis `NEXT_PUBLIC_*`.
- Nunca publique a service role key do Supabase no navegador.
- Configure URLs de redirecionamento do Supabase.
- Teste RLS com duas empresas diferentes antes de aceitar clientes.
- Configure termos, política de privacidade e processos LGPD com revisão profissional.
