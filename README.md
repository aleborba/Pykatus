Módulo Akatus para integração com Python
==========================================

Author: Alê Borba

Version: v0.0.4

ChangeLog:
-----------
0.0.4
* Implentação de validators()
* Refatoração na geração do XML

0.0.3
* Testes para a geração do XML

0.0.2
* Validação de campos vazios.
* Inclusão de testes para checagem de parametros vazios.

Como usar
-------------------------

from pykatus import Akatus

akatus = Akatus()

akatus.set_ambiente("sandbox")

akatus.set_recebedor("seu_token", "seu_email")

akatus.set_pagador("nome_pagador", "email_do_pagador", "tipo_do_telefone", "1109940566")

akatus.set_produto("codigo", "descricao", "qtdade", "preco", "peso", "frete", "desc")

akatus.set_transacao("desc_total", "peso_total", "frete_total", "BRL", "ref", "meio_de_pagamento")

akatus.envia()

print akatus.get_resposta()

ToDo
----------------
* Validar melhor os campos
* Tratar melhor os erros
* Melhorar os testes automatizados
* Opção de incluir mais de um produto
