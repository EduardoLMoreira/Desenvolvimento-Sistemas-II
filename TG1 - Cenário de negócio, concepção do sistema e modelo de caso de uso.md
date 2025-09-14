# TG1 – Cenário de negócio, concepção do sistema e modelo de caso de uso

## 2.3 Casos de uso resumidos
Cada caso é descrito em parágrafo único: **Ator… Sistema…**

| ID  | Nome            | Resumo |
|-----|-----------------|--------|
| UC01| Agendar serviço | **Cliente** agenda um serviço informando veículo e data; o **Sistema** registra a solicitação. |
| UC02| Check-in veículo| **Atendente** registra a chegada do veículo; o **Sistema** armazena quilometragem e observações. |
| UC03| Gerar orçamento | **Atendente** solicita cálculo; o **Sistema** gera proposta de serviços, peças e prazos. |
| UC04| Aprovar orçamento| **Cliente** avalia proposta; o **Sistema** registra aprovação ou recusa. |
| UC05| Emitir OS       | **Chefe de Oficina** confirma orçamento aprovado; o **Sistema** cria a Ordem de Serviço. |
| UC06| Registrar serviços | **Mecânico** registra serviços executados; o **Sistema** atualiza a OS. |
| ... | ...            | (continue demais casos nesse padrão) |

## 2.4 Especificação detalhada – UC04

**Objetivo**: Registrar a aprovação do orçamento.

**Atores**: Cliente, Sistema.

**Pré-condição**: Orçamento gerado e pendente de aprovação.

**Fluxo principal**  
1. Cliente acessa o orçamento.  
2. Cliente escolhe aprovar.  
3. Sistema registra aprovação.  
4. *Inclui UC05 – Emitir OS*.

**Fluxos alternativos**  
A1 – Cliente solicita ajuste …  
A2 – Orçamento expirado …

**Fluxos de exceção**  
E1 – Link inválido …  
E2 – Falha de autenticação …

## 2.5 Diagrama de Caso de Uso
![Diagrama de Caso de Uso](images/caso-uso.png)
