O que devo fazer?

Veja essa tabela e escreva a query pedida no fim:

Tabela - provas
Colunas:
id_aluno  - número
id_materia  - número
 nota  - número flutuante
 data_da_prova  data

Tabela - aluno
 colunas:
 id numero
 nome string
 data_nascimento numero

Tabela - professor
 colunas:
 id numero
 nome string
 data_nascimento numero

Tabela - materia
 colunas:
 id numero
 nome string
 id_professor numero


 Crie 3 alunos;
 Crie uma matéria e um professor;
 Crie 1 prova para cada aluno nessa matéria e diga que nota eles tiraram.

 


# Tabelas_em_Query

# Organização do Banco de Dados para Sistema de Provas

## Estrutura das Tabelas

### Tabela - aluno
- `id` (número, PK)
- `nome` (string)
- `data_nascimento` (data)

### Tabela - professor
- `id` (número, PK)
- `nome` (string)
- `data_nascimento` (data)

### Tabela - materia
- `id` (número, PK)
- `nome` (string)
- `id_professor` (número, FK)

### Tabela - provas
- `id_aluno` (número, FK)
- `id_materia` (número, FK)
- `nota` (número flutuante)
- `data_da_prova` (data)

## Inserção de Dados

### Criar 3 alunos

INSERT INTO aluno (id, nome, data_nascimento) VALUES
(1, 'João Silva', '2000-01-15'),
(2, 'Maria Oliveira', '2001-05-22'),
(3, 'Carlos Souza', '1999-11-30');

### Criar um professor
INSERT INTO professor (id, nome, data_nascimento) VALUES
(1, 'Ana Pereira', '1980-03-10');

### Criar uma matéria
INSERT INTO materia (id, nome, id_professor) VALUES
(1, 'Matemática', 1);


### Criar uma prova para cada aluno nessa matéria
INSERT INTO provas (id_aluno, id_materia, nota, data_da_prova) VALUES
(1, 1, 8.5, '2024-11-15'),
(2, 1, 9.0, '2024-11-15'),
(3, 1, 7.5, '2024-11-15');
