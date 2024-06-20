# Como acessamos o valor de um atributo dentro de um dicionário em nossos templates?

- [ ] {{nome_do_dicionario_nome_do_atributo}}.
- [x] {{nome_do_dicionario_nome_do_atributo}}.
- [ ] {{nome_do_dicionario_nome_do_atributo}}.
- [ ] {{nome_do_dicionario_nome_do_atributo}}.
- [ ] {{nome_do_dicionario_nome_do_atributo}}.

<hr>

# Como fazemos para exibir informações de uma variável Python dentro de um template Django?

- [x] {{nome_da_variavel}}.
- [ ] ((nome_da_variavel)).
- [ ] {%nome_da_variavel%}.
- [ ] %%nome_da_variavel%%.
- [ ] {nome_da_variavel}.
<hr>

# Qual template tag utilizamos para criar blocos de comentários nos templates do Django?

- [ ] Conteúdo do comentário {% endcomment %}`.
- [x] {% comment %} Conteúdo do comentário {% endcomment %}.
- [ ] {% comment %} Conteúdo do comentário {% end %}.
- [ ] {% comment %} Conteúdo do comentário {% comment %}.
- [ ] {% comment %} Conteúdo do comentário.
<hr>

# Qual template tag utilizamos para criar rotas nos templates do Django?

- [ ] {% urls 'nome_da_rota' %}.
- [ ] {{ url 'nome_da_rota' }}.
- [ ] {% http 'nome_da_rota' %}.
- [x] {% url 'nome_da_rota' %}.
- [ ] {% route 'nome_da_rota' %}.
<hr>

# Observe o código abaixo?

```
# views.py
def index(request):
    nome_da_empresa = "TreinaWeb"
    descricao_da_empresa = "Há mais de 12 anos formando desenvolvedores de ponta! São mais de 4.000 horas de conteúdo, com formações completas e com foco no mercado de trabalho."


    cursos_home = {

    }

    return render(request, 'empresa/index.html', {'nome_empresa':nome_da_empresa, 'descricao_empresa':descricao_da_empresa,
                                                  'cursos_home':cursos_home})
-------------------
# index.html
<div class="row">
  {% for curso_id, curso in cursos_home.items %}
  <div class="col-md-4 mb-5">
    <div class="card h-100">
      <img class="card-img-top" src="http://placehold.it/300x200" alt="">
      <div class="card-body">
          <h4 class="card-title">{{curso_id}} - {{curso.titulo}}</h4>
        <p class="card-text">{{curso.descricao}}</p>
      </div>
      <div class="card-footer">
        <a href="#" class="btn btn-primary">Find Out More!</a>
      </div>
    </div>
  </div>
  {% empty %}
    <h3>Novos cursos serão lançados em breve</h3>
  {% endfor %}
</div>
```



- [ ] O que será impresso quando o arquivo index.html for renderizado?

- [x] A mensagem "Novos cursos serão lançados em breve".

- [ ] O titulo e descrição de todos os cursos.

- [ ] O titulo de todos os cursos.

- [ ] O id, titulo e descrição de todos os cursos.

- [ ] Nada, pois haverá um erro de execução no código.

- [ ] O id, e descrição de todos os cursos.
<hr>

# Qual template tag utilizamos para repetir um determinado bloco de código no sistema de templates do Django?

- [ ] {% loop %}.
- [ ] {% while %}.
- [ ] {% do while %}.
- [ ] {% forloop %}.
- [x] {% for %}.
<hr>

# Observe o código abaixo:



```
{% for curso_id, curso in cursos_home %}
<div class="col-md-4 mb-5">
  <div class="card h-100">
    <img class="card-img-top" src="http://placehold.it/300x200" alt="">
    <div class="card-body">
      <h4 class="card-title">{{curso_id}}</h4>
    </div>
    <div class="card-footer">
      <a href="#" class="btn btn-primary">Find Out More!</a>
    </div>
  </div>
</div>
{% endfor %}

```
Partindo do pressuposto que a variável cursos_home possui outros dicionários armazenados, o que será exibido após sua execução?

- [ ] Será exibido os ids dos cursos existentes no dicionário cursos_home.
- [x] Não será exibido nada, já que a forma que iteramos o dicionário cursos_home está incorreta.
- [ ] Será exibido os titulos dos cursos existentes no dicionário cursos_home.
- [ ] Será exibido os cursos existentes no dicionário cursos_home.
- [ ] Será exibido o id do primeiro curso existente no dicionário cursos_home.

<hr>

# Qual template tag utilzamos para criar uma execução condicional no sistema de template do Django?

- [x] {% if %}.
- [ ] {% if_django %}.
- [ ] {% case %}.
- [ ] {% switch %}.
- [ ] {% conditional %}.
- [ ] {% else %}.
<hr>

# Qual template tag utilzamos para não exibir dados imediatamente iguais no DTL?

- [ ] {% case %}.
- [ ] {% switch %}.
- [X] {% ifchanged %}.
- [ ] {% else %}.
- [ ] {% if_django %}.
- [ ] {% conditional %}.
<hr>

# Qual sintaxe utilizada para o uso de filtros no Django Templates?

- [x] {{nome_da_variavel|nome_do_filtro}}.
- [ ] {{nome_do_filtro|nome_da_variavel}}.
- [ ] {{nome_da_variavel/nome_do_filtro}}.
- [ ] {{nome_da_variavel?nome_do_filtro}}.
- [ ] {% if_django %}.
- [ ] {{nome_da_variavel:nome_do_filtro}}.
<hr>

# Qual filtro utilizado para transformar todos os caracteres de uma palavra (ou frase) em maiúsculo?

- [ ] maiusculum.
- [ ] upp.
- [x] upper.
- [ ] size.
- [ ] lower.
<hr>