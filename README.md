# ORION — Evolução 1 (Streamlit)

Esta é uma cópia experimental separada da versão existente. **Não substitua o `app.py` em produção antes de testar.**

## O que esta etapa acrescenta
- Modos de resposta: Automático, Pesquisa e atualidades, Estudo e explicação, Programação e tecnologia, Criatividade.
- Instruções de qualidade para contexto, incerteza, segurança e não inventar pesquisas/ações.
- Controle para ativar/desativar a leitura das respostas com Cartesia.
- Exportação da conversa ativa em JSON ou TXT.
- Mensagem de erro mais segura na interface, sem mostrar diretamente exceções potencialmente sensíveis.
- Mantém a base de login, Supabase, memória, pesquisa do Groq, voz Cartesia e renderização matemática do arquivo-base.

## O que NÃO foi alterado ou adicionado nesta etapa
- Não substitui o modelo Groq nem conecta APIs de outros fornecedores.
- Não adiciona visão por câmera, controle do computador, automação externa ou memória nova.
- Não muda o banco Supabase nem exige novas tabelas.
- A pesquisa continua dependendo da ferramenta `browser_search` que já existia no arquivo-base e da compatibilidade do modelo/conta Groq.

## Teste seguro
1. Baixe e extraia o ZIP.
2. Copie `app_orion_evolucao_v1.py` para uma pasta de teste do seu repositório.
3. No Streamlit Cloud, crie um app de teste apontando para esse arquivo, ou teste localmente com o mesmo ambiente e os Secrets existentes.
4. Não publique `secrets.toml`, `.env` ou chaves no GitHub.
5. Teste login, memória, pesquisa atual, voz Cartesia, renderização matemática e exportação de conversas.
6. Só depois de validar tudo decida se quer substituir a versão principal. Mantenha o `app.py` atual intacto até lá.

## Secrets
O código usa os nomes já esperados pela versão-base, por exemplo `GROQ_API_KEY`, `SUPABASE_URL`, `SUPABASE_KEY` e, para voz, `CARTESIA_API_KEY` e `CARTESIA_VOICE_ID`. Configure-os na área Secrets do Streamlit; não os coloque no código.

## Verificação feita
- Sintaxe Python validada com `py_compile`.
- Não foi possível validar chamadas reais a Groq, Supabase ou Cartesia sem executar no seu ambiente e sem suas credenciais privadas.
