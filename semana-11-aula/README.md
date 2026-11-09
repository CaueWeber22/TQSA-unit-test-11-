# Persistência de alunos com mock do MongoDB

Solução da atividade baseada no [código fornecido em aula](https://github.com/TQSA6/semana-11-aula).

O método `AlunoClass.salvar` insere uma cópia dos atributos do aluno na coleção
informada e retorna a confirmação da inserção. A cópia evita que o campo `_id`
adicionado pelo MongoDB seja incluído nos atributos do objeto original.

O teste `alunoTest.test_salvarAluno` utiliza a conexão simulada pelo `mongomock`
no `setUp`. Ele verifica a confirmação do salvamento, a quantidade de documentos,
os campos persistidos e a preservação dos atributos do aluno. Não é necessário
instalar ou iniciar um servidor MongoDB.

## Executar

Com Python instalado, execute nesta pasta:

```powershell
python -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
.\.venv\Scripts\python.exe -m unittest -v testes
```

O comando executa tanto o teste do aluno quanto o teste de turma fornecido no exemplo.
