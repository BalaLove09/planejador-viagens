# Planejador de Viagens

Trabalho final da disciplina de Programação Web (Angular).

## Domínio
Aplicação para planejar viagens. O usuário cadastra suas viagens (destino, período e orçamento) e registra as atividades de cada uma (passeios, transporte, hospedagem, alimentação), com data e custo. É possível consultar, editar e remover viagens e atividades, acompanhar quanto do orçamento já foi comprometido e marcar atividades como concluídas, vendo o progresso de cada viagem.

## Entidades
| Entidade | Atributos | Relacionamento |
|---|---|---|
| Viagem | id, destino, dataInicio, dataFim, orcamento | Uma viagem possui várias atividades (1:N) |
| Atividade | id, titulo, categoria, data, custo, concluida, viagemId | Cada atividade pertence a uma única viagem |

- `categoria`: Transporte, Hospedagem, Passeio ou Alimentação
- `concluida`: booleano, começa como `false`

## Funcionalidades adicionais
- **Resumo de orçamento:** total gasto, saldo restante e alerta quando o total ultrapassa o orçamento, atualizados automaticamente.
- **Conclusão de atividades:** botão alterna pendente/concluída; barra de progresso com o percentual concluído por viagem.

## Biblioteca externa
- [ngx-mask](https://github.com/JsDaddy/ngx-mask): máscara de moeda (R$) nos campos de orçamento e custo.
