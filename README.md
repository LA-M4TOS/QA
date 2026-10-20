📘 README.md — Mova Studio Database as Code
🏷️ Sobre o Projeto
Este repositório contém a definição do esquema de banco de dados utilizando o conceito Database as Code, gerenciado pelo Mova Studio.
Toda a estrutura do banco é versionada em arquivos YAML, permitindo rastreabilidade, auditoria e colaboração via Git.

📂 Estrutura do Repositório
Código
/schema.yaml        # Definição principal do banco de dados
/tables/            # Tabelas adicionais (se aplicável)
/functions/         # Funções SQL (opcional)
/aggregates/        # Aggregates configurados no Mova (opcional)
/migrations/        # Scripts gerados automaticamente (opcional)
🧩 Arquivo principal: schema.yaml
O arquivo schema.yaml contém:

Metadados do banco

Versão do schema

Configuração do tipo de banco (ex.: SQL Server, PostgreSQL, etc.)

Definição das tabelas

Colunas, tipos, chaves primárias e restrições

Exemplo simplificado:

yaml
metadata:
  name: MyDatabase
  version: 1.0.0
  database: sqlserver
  author: User

tables:
  - name: ExampleTable
    columns:
      - name: id
        type: int
        primary_key: true
      - name: name
        type: nvarchar(255)
        nullable: false
🔄 Fluxo de Trabalho (Git)
O Mova Studio utiliza Git para versionamento. O fluxo recomendado é:

Editar o schema no editor do Mova.

Commit local das alterações.

Push para o repositório remoto.

⚠️ Possíveis erros comuns
“Commit realizado localmente, mas o push falhou”
Este erro ocorre quando:

Existem alterações mais recentes no repositório remoto

A branch local está desatualizada

Credenciais Git não estão configuradas corretamente

Solução:

Atualize a branch (pull)

Verifique o token/credencial Git nas configurações do repositório

🚀 Deploy / Aplicação do Schema
O Mova Studio permite:

Aplicar o schema diretamente no banco

Gerar scripts de migração

Validar alterações antes de aplicar

👥 Contribuição
Alterações no schema devem seguir:

Commits claros e descritivos

Revisão antes do push

Validação do plano de alterações no Mova Studio

🛡️ Boas Práticas
Sempre sincronize a branch antes de iniciar alterações

Evite editar YAML fora do Mova Studio

Utilize descrições nas tabelas e colunas

Mantenha a versão do schema atualizada

📞 Suporte
Para dúvidas sobre o Mova Studio, consulte:

Documentação interna

Equipe responsável pelo projeto

testes

Administradores do repositório Git

teste subindo no GITHUB