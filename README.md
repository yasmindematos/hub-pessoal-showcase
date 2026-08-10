# 💜 Hub Pessoal — projeto privado

> Repositório de vitrine. O código-fonte e o site ficam em ambiente privado por conterem dados pessoais.

## O que é

Um web app pessoal de organização de vida que centraliza, em um só lugar:

- 💰 **Finanças**: controle de entradas e saídas do mês, por categoria, e planejamento de objetivos de investimento com barras de progresso e registro de aportes
- 🏗️ **Imóvel na planta**: acompanhamento da evolução da obra e do cronograma de parcelas da entrada, com cálculo automático da correção paga (previsto vs. real)
- 📚 **Estudos**: cursos e MBA organizados em matérias, cada uma com anotações datadas e links de referência com prévia automática de imagens e vídeos
- 💼 **Trabalho**: tarefas por produto com status, anotações de reuniões e biblioteca de links úteis
- 🫶 **Diário de sentimentos**: registro de humor com escala visual e texto livre

## Stack

| Camada | Tecnologia |
|---|---|
| Front-end | React + Vite |
| Autenticação | Supabase Auth (cadastros desativados, usuária única) |
| Banco de dados | Supabase (PostgreSQL) com Row Level Security |
| Hospedagem | Vercel |
| Design | Design tokens próprios, paleta roxo + verde oliva + lilás, tipografia Bricolage Grotesque + Instrument Sans + JetBrains Mono |

## Decisões de produto e segurança

- **Privacidade por arquitetura**: políticas de RLS garantem no nível do banco que cada linha só é lida e escrita pela dona da conta, independentemente do front-end.
- **Segredos fora do repositório**: credenciais vivem em variáveis de ambiente (local e Vercel), nunca no código.
- **Modelo de dados flexível**: cada área do hub é um documento JSON versionável por seção, o que permite evoluir funcionalidades sem migrações pesadas.
- **UX otimista**: a interface atualiza na hora e persiste em segundo plano, com aviso em caso de falha de rede.

## Por que esse projeto existe

Nasceu da vontade de juntar planejamento financeiro, o acompanhamento de um apê comprado na planta, estudos de produto e IA, trabalho e bem-estar em uma ferramenta única, do meu jeito, em vez de espalhar a vida em cinco apps diferentes. Também foi meu laboratório prático de autenticação, segurança de dados e deploy contínuo.

---

*Feito com muito 💜 (e verde oliva).*
