# Algoritmos_e_Estruturas_de_dados_projeto_final_BICT_2025

# Projeto final

# Painel de controle de uma biblioteca

1. Problema para resolver (Inovação)
   
 Nas bibliotecas tradicionais, o gerenciamento de recursos (livros, computadores, equipamentos) é feito manualmente ou com sistemas simples que não consideram prioridade, urgência, reservas futuras ou modo de operação emergencial.
O problema a ser resolvido é criar um sistema que:

- Organize usuários e recursos.

- Permita entrada em fila com prioridade automática para professores e casos urgentes.

- Gerencie reservas para horários futuros.

- Ative modo emergência para reorganizar prioridades em períodos críticos (como semanas de prova).

- Gere estatísticas de uso para auxiliar na gestão.

2. Roteiro para resolver (Criação)
   
- Analisar requisitos:

Cadastro de usuários e recursos.

Entrada em fila com prioridade.

Controle de reservas.

Estatísticas.

Modo emergência.

- Escolher estruturas de dados

Listas para armazenar usuários, recursos e reservas.

Fila de prioridade (heapq) para gerenciar ordem de atendimento.

Dicionário (dict) para mapear recurso → fila.

- Definir fluxo do sistema

Quando um recurso estiver disponível → alocar imediatamente.

Quando indisponível → inserir na fila de prioridade.

Permitir reservas futuras com checagem de horário.

Ajustar prioridades quando o modo emergência for ativado.

- Criar classes para organização

Usuario → dados do usuário.

Recurso → dados do recurso.

SistemaBiblioteca → gerencia toda a lógica.

- Implementar e testar

Simular cenários com estudantes, professores, urgência e reservas.

Validar estatísticas.

3. Estruturas de dados utilizadas
   
- Estrutura	Uso no código
  
Lista (list)	Armazena todos os usuários (self.usuarios), recursos (self.recursos) e reservas (self.reservas).
Heap (heapq)	Implementa a fila de prioridade para uso de recursos (self.filas[recurso]).
Dicionário (dict)	Associa cada recurso à sua respectiva fila (self.filas).
Classe	Estrutura cada entidade (Usuario, Recurso, SistemaBiblioteca).

5. Script – Implementação (Resumo)
   
- Classes principais
  
Usuario → nome, tipo (0 = estudante, 1 = professor), área.

Recurso → tipo (livro, computador, etc.), nome e quantidade disponível.

SistemaBiblioteca:

Cadastro de usuários e recursos.

Entrada em fila com prioridade calculada.

Reservas com data/hora de início e fim.

Modo emergência que altera prioridade.

Estatísticas de uso.

 Resumo do que o código simula:

Cria o sistema.

Cadastra usuários e recursos.

Processa usos imediatos.

Faz uma reserva para o futuro.

Ativa um modo de atendimento prioritário.

Gera um relatório de estatísticas.
