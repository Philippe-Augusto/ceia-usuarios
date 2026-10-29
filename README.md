# ceia-usuarios

Solicitação de acesso aos clusters HPC do CEIA/Akcit.

## Como pedir acesso

1. Abra uma [nova issue](../../issues/new/choose) e escolha o formulário:
   - **Solicitação de Acesso a Cluster HPC**: primeiro acesso. Anexe o Termo de Responsabilidade assinado (PDF).
   - **Solicitação de Acesso Adicional**: você já tem usuário e precisa de outro cluster.
2. Se faltar algum dado, um comentário automático indica o que corrigir. Edite a issue (`...` → **Edit**).
3. Depois da aprovação, você recebe por email o usuário, a senha temporária, o arquivo da VPN e o link do manual.
   No primeiro login a senha temporária precisa ser trocada.

Não coloque senhas nem dados sensíveis além do que o formulário pede: **as issues são públicas**.

## Para administradores

| Workflow | Quando roda | O que faz |
|---|---|---|
| `validar-issue.yml` | issue aberta/editada | confere os campos e o anexo; fecha issues sem formulário |
| `atualizar-titulo-issue.yml` | issue aberta/editada | padroniza o título e cria o checklist ("Email enviado") |

Labels: `novo-acesso` / `acesso-cluster-adicional` (tipo), `pendente`, `dados-pendentes`.

Ao marcar "Email enviado" no checklist, o workflow registra a data e quem marcou.

O usuário é criado por um administrador, fora do GitHub. Nenhuma senha fica neste repositório, e os logs
das Actions são públicos. O passo a passo está no repositório interno de infraestrutura.
