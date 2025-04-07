# Guia de Contribuição

Abaixo você pode encontrar as diretrizes para poder fazer sua contribuição com o projeto MundoMusical, descrevendo detalhadamente como proceder ao criar issues, commits, pull requests, branches e comentários no código.

## Issues


### Criaçaõ de Issues

- Título: um resumo do problema ou sugestão que está sendo criado.
- Descrição: incluindo passos para reprodução, contexto detalhado, comportamento esperado e comportamento atual observado. Sempre que possível, adicione capturas de tela, logs ou trechos de código que ajudem a ilustrar o problema.

### Uso de Templates

Utilize os templates de acordo com cada tipo de issue:

- Bug report: reportar bugs ou falhas.
- Feature request: sugerir uma nova funcionalidade.
- Task: para qualquer issue que não se adeque as outras criadas.

## Commits
Siga o padrão:

```
<tipo>: <descrição breve>
```
### Tipos de commit
Padrão de prefixo (conventional commits):

- **feat**: nova funcionalidade.

- **fix**: correção de bug.

- **docs**: alterações na documentação

- **style**: ajustes de formatação, sem alteração de código

- **refactor**: refatoração de código, sem alterar funcionalidade

- **test**: adição ou modificação de testes

- **chore**: tarefas de build, scripts, dependências etc.

### Exemplos:

feat(login): adiciona autenticação com Google

fix(api): corrige erro de timeout ao buscar dados do usuário

docs(readme): adiciona instruções de instalação

refactor: renomeia funções para melhorar legibilidade

chore: atualiza dependências do projeto

## Pull Request

### Estrutura de Pull Requests para Código

- **Título**: Seja objetivo sobre o conteúdo modificado ou criado.
- **Descrição**:
  - **O que foi feito**: Descreva as mudanças realizadas.
  - **Por que foi feito**: Explique a motivação por trás das mudanças.
  - **Como testar**: Instruções para testar as alterações.

### Estrutura de Pull Requests para Documentos

- **Título**: Seja objetivo sobre o conteúdo modificado ou criado.
- **Descrição**:
  - **Resumo**: Descreva brevemente as mudanças.
  - **Referências**: Inclua links ou menções relevantes.

## Estrutura de Branches

Use o seguinte padrão para nomear branches:

```
<numero_da_issue>-<descricao->
```

### Exemplo

- Para a issue **#3 Criação documento de BPMN**:

  ```
  3-criacao-documento-de-bpmn
  ```

  ## Comentários no Código

### Boas Práticas

- **Seja claro e objetivo**  
  Comente trechos que possam causar dúvidas futuras. O comentário deve explicar o *porquê*, não apenas o *o quê*.

- **Evite o óbvio**  
  Comentários redundantes apenas poluem o código. Exemplo a evitar:  
  `i += 1  # incrementa i em 1`

- **Mantenha os comentários atualizados**  
  Comentários desatualizados são piores que a ausência deles, pois confundem quem lê o código.

---

### Padronização

- **Funções e Classes**  
  Utilize *docstrings* (em Python) ou comentários estruturados (em outras linguagens) para documentar:
  - O propósito da função ou classe
  - Parâmetros esperados
  - Valor de retorno

- **TODOs**  
  Utilize `// TODO:` ou `# TODO:` para sinalizar tarefas pendentes no código.

- **FIXME**  
  Utilize para destacar trechos de código que requerem atenção ou correção futura.

---

### Exemplo (em Python)

```python
def calcular_media(valores):
    """
    Calcula a média aritmética de uma lista de números.

    Parâmetros:
    valores (list[float]): Lista de números.

    Retorno:
    float: Média aritmética dos valores.
    """
    if not valores:
        return 0 

    soma = sum(valores)
    total = len(valores)

    return soma / total

# TODO: Validar se todos os valores são numéricos antes do cálculo
```