# Fabio Manutenções — Portal de Chamados

Projeto acadêmico desenvolvido para o Projeto Integrado de **Interface Humano-Computador e Estatística**, do curso de Análise e Desenvolvimento de Sistemas da **UNIFEOB**.

O portal demonstra uma solução para registrar solicitações de manutenção, acompanhar atendimentos e consultar indicadores de qualidade.

> Esta versão é uma demonstração. Os clientes e chamados são fictícios, a autenticação é simulada e os dados são reiniciados ao recarregar a página.

## Contexto do projeto

A empresa parceira, Fabio Manutenções, atua principalmente na instalação e manutenção de sistemas de ar condicionado, ventilação e refrigeração.

Atualmente, as solicitações chegam pelo WhatsApp. Fabio trabalha principalmente sozinho, contando eventualmente com um ajudante.

A proposta é reunir as informações dos atendimentos em uma interface simples, acessível pelo celular ou computador, apoiando a consulta de pendências e o acompanhamento dos serviços.

## Objetivos

- Facilitar o registro e o acompanhamento de chamados.
- Organizar situações, prioridades e informações dos atendimentos.
- Registrar diagnósticos e identificar ocorrências repetidas em equipamentos.
- Apresentar indicadores de qualidade com gráficos e valores.
- Aplicar conceitos de usabilidade e estatística descritiva.

## Funcionalidades

### Área do cliente

- Acesso com usuário e senha de demonstração.
- Consulta dos próprios chamados.
- Registro de novas solicitações.
- Acompanhamento da situação e do resumo do atendimento.
- Solicitação de retorno quando o problema continua.

### Área administrativa

- Consulta, pesquisa e filtros de chamados.
- Cadastro de novos acessos de clientes.
- Atualização de situação, prioridade e agendamento.
- Identificação do equipamento e de quem executou o serviço.
- Registro do diagnóstico e da primeira verificação.
- Classificação dos motivos de retorno.
- Consulta de indicadores e gráficos.

### Situações dos chamados

- Novo
- Agendado
- Em atendimento
- Aguardando retorno
- Concluído

## Estatística e qualidade

A demonstração utiliza uma base inicial de **30 chamados fictícios**, distribuídos entre **oito clientes**.

O painel apresenta:

- Quantidade de chamados pendentes.
- Quantidade de chamados aguardando retorno.
- Frequência e participação percentual das falhas diagnosticadas.
- Moda das falhas.
- Percentual de aprovação na primeira verificação.
- Proporção de retornos classificados como mesmo problema.
- Equipamentos com ocorrências repetidas.
- Quantidade de primeiras conclusões por semana.
- Média, mediana e desvio-padrão populacional do volume semanal.

### Regras dos indicadores

A primeira verificação é preservada para que alterações posteriores não apaguem seu resultado.

Cada chamado é contado apenas uma vez no resumo semanal, considerando sua primeira conclusão. Semanas completas sem conclusões entram no cálculo com valor zero.

Um retorno pode representar o mesmo problema, uma nova falha ou uma visita planejada. Portanto, nem todo retorno significa retrabalho.

Os indicadores demonstram os conceitos estatísticos do projeto e **não representam o desempenho real da empresa**.

## Interface Humano-Computador

A interface foi planejada para facilitar tarefas frequentes e reduzir o esforço de preenchimento.

Entre as decisões adotadas estão:

- Separação das áreas de cliente e administrador.
- Linguagem direta e próxima da rotina de manutenção.
- Padrões consistentes de navegação e formulários.
- Confirmações após ações e mensagens de erro.
- Situações identificadas por texto e cor.
- Gráficos acompanhados de valores e legendas.
- Layout responsivo para celular e computador.

A identidade visual utiliza o logotipo fornecido para o projeto e uma paleta baseada em azul escuro, azul, azul claro e dourado.

## Tecnologias

- HTML5
- CSS3
- JavaScript
- SVG para elementos gráficos
- Figma para a apresentação do protótipo

A demonstração web não utiliza framework nem exige uma etapa de compilação.

## Estrutura do repositório

```text
.
├── index.html
├── style.css
├── app.js
├── assets/
│   └── identidade-fabio.png
├── netlify.toml
└── README.md
```

## Como executar

### Abrindo no navegador

Baixe ou clone o repositório e abra o arquivo `index.html`.

Mantenha os demais arquivos e a pasta `assets` na mesma estrutura.

### Usando um servidor local

Com Python 3 instalado, execute na pasta do projeto:

```bash
python3 -m http.server 4173
```

Depois, acesse:

```text
http://localhost:4173
```

Para encerrar o servidor, pressione `Ctrl + C` no terminal.

## Acessos de demonstração

### Administrador

| Usuário | Senha |
|---|---|
| admin | 123456 |

### Clientes fictícios

Todos os clientes abaixo utilizam a senha `1234`.

| Cliente | Usuário |
|---|---|
| Pararia queijo | pqueijo |
| Açougue Sivla | asilva |
| Mercado Limeira | mlimeira |
| Restaurante Sabor Caseiro | rsaborcaseiro |
| Frios Primavera | fprimavera |
| Sorveteria Estação | sestacao |
| Oficina São Pedro | osaopedro |
| Hortifruti Boa Colheita | hboacolheita |

As credenciais estão no código para permitir a demonstração acadêmica. Não devem ser reutilizadas em um sistema de produção.

## Sugestão de teste

1. Entre com um perfil de cliente.
2. Registre um chamado com dados fictícios.
3. Clique em **Sair**, sem recarregar a página.
4. Entre com o usuário `admin`.
5. Localize o chamado e atualize o atendimento.
6. Informe diagnóstico, primeira verificação e data de conclusão.
7. Entre novamente como cliente para acompanhar o resultado.
8. Consulte os gráficos na área administrativa.

## Limitações da versão

- Os dados ficam apenas na memória do navegador.
- Recarregar a página restaura os exemplos iniciais.
- Não existe banco de dados conectado.
- O login e a separação dos perfis são simulados no navegador.
- Não há proteção adequada para armazenar dados reais de clientes.
- Nenhuma solicitação é enviada automaticamente ao Fabio.
- Não existe integração automática com WhatsApp ou Google Forms.
- A demonstração não inclui pagamentos, emissão fiscal ou controle de estoque.

A presença do arquivo `netlify.toml` não significa que o site já esteja publicado.

## Possíveis evoluções

- Autenticação real e controle de acesso no servidor.
- Persistência dos dados em banco de dados.
- Publicação para acesso por link.
- Histórico das alterações dos chamados.
- Notificações de atualização.
- Melhorias a partir de testes com Fabio e clientes.
- Avaliação de acessibilidade.

Netlify e Supabase foram considerados para uma futura implantação, mas não estão integrados nesta versão.

## Protótipo no Figma

Adicionar aqui o link compartilhável do protótipo.

## Autoria

Projeto desenvolvido por **Thiago Correa**.

Curso de Análise e Desenvolvimento de Sistemas — **UNIFEOB**.

Empresa parceira: **Fabio Manutenções**.
