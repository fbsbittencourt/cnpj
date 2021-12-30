<h1 align='center'>
CNPJ API v1.1
</h1>

<a href='http://cn-pj.tech/api'>
  <img src='https://logodownload.org/wp-content/uploads/2014/11/receita-federal-logo-1.png'/>
</a>

<p align='center'>
  <a href='http://cn-pj.tech/api'><img src='https://img.shields.io/badge/Atualiza%C3%A7%C3%A3o-22/12/2021-blue'/></a>
</p>

<p align="center">⭐️ Deixe uma estrela ⭐️</p>

<a align='center' href='http://cn-pj.tech/api'>

`GET /api`

</a>

```json
{
  "msg_ver": "CNPJ API v1.1",
  "ult_att": "22/12/2021",
  "url_api": "http://cn-pj.tech/api/00000000000191"
}
```

<table align='center'>

<tr><th>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Grátis&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</th><th>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Paga&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</th></tr>
<tr><td align='center'>

 <a href='http://cn-pj.tech/api/00000000000191'>`GET /api/:cnpj`</a>

 Autenticação | Limite
:-:|:-:
Não|100/dia

</td><td align='center'>

 <a href='http://cn-pj.tech/api2/00000000000191?token=...'>`GET /api2/:cnpj?token=…`</a>

 Autenticação | Limite
:-:|:-:
Sim|Sem limites

</td></tr> </table>


```json
{
  "cnpj": "13347016000117",
  "matriz_filial": "Matriz",
  "razao_social": "FACEBOOK SERVICOS ONLINE DO BRASIL LTDA.",
  "nome_fantasia": null,
  "cod_natureza_juridica": 2062,
  "natureza_juridica": "Sociedade Empresária Limitada",
  "porte": "DEMAIS",
  "simples": {
    "optante": false,
    "data_opcao": null,
    "data_exclusao": null
  },
  "mei": {
    "optante": false,
    "data_opcao": null,
    "data_exclusao": null
  },
  "data_inicio_ativ": "14/02/2011",
  "situacao_cadastral": "ATIVA",
  "data_situacao_cadastral": "14/02/2011",
  "motivo_situacao_cadastral": "SEM MOTIVO",
  "cnae_principal": {
    "7312200": "Agenciamento de espaços para publicidade, exceto em veículos de comunicação"
  },
  "cnae_secundaria": {
    "7020400": "Atividades de consultoria em gestão empresarial, exceto consultoria técnica específica",
    "7319004": "Consultoria em publicidade"
  },
  "contato": {
    "ddd": "11",
    "tel": "30736800",
    "email": "TAXCOMPLIANCEBR@FB.COM"
  },
  "endereco": {
    "cep": "4542000",
    "uf": "SP",
    "cod_municipio": 7107,
    "municipio": "SAO PAULO",
    "bairro": "ITAIM BIBI",
    "tipo_logadouro": "RUA",
    "logadouro": "LEOPOLDO COUTO DE MAGALHAES JUNIOR",
    "numero": "700",
    "complemento": "ANDAR 1/5/6/9/14 E 15     EDIF  INFINITY"
  },
  "qsa": [
    {
      "ident": "PESSOA JURÍDICA",
      "doc": "22576790000190",
      "nome": "FACEBOOK MIAMI, INC.",
      "data_entrada": "17/09/2015",
      "qualificacao": "Sócio Pessoa Jurídica Domiciliado no Exterior",
      "idade": "Não se aplica"
    },
    {
      "ident": "PESSOA FÍSICA",
      "doc": "***634408**",
      "nome": "CONRADO LEISTER",
      "data_entrada": "14/11/2018",
      "qualificacao": "Administrador",
      "idade": "41-50 Anos"
    }
  ]
}
```

<h1 align='center'>
Exemplo de uso com Python
</h1>

<p align='center'>Sem token</p>

```python
from requests import get

data = get('http://cn-pj.tech/api/13347016000117').json()

cnpj = data['cnpj']
nome = data['razao_social']

print(cnpj, nome)
```


<p align='center'>Com token</p>

```python
from requests import get

data = get(f'http://cn-pj.tech/api2/13347016000117?token={TOKEN}').json()

cnpj = data['cnpj']
nome = data['razao_social']

print(cnpj, nome)
```

> Para melhor visualização dos dados no navegador:
> 
> https://chrome.google.com/webstore/detail/json-viewer/gbmdgpbipfallnflgajpaliibnhdgobh?hl=pt-BR
>
> Dados atualizados conforme atualização do banco de dados da Receita Federal.
> 
> Mais info: gabriel-tavares2009@hotmail.com
> 
