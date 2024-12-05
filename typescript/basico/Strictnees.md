No typescript podemos controlar o nível de rigor de suas validações. Por si só o typescript é bem permissivo mas ativando a flag --strict no CLI, ou "strict"=true no ts.config nos podemos ativar todos os rigores disponíveis. Sendo possível desativar individualmente.

## NoImplicityAny
Uma strict que evita que valores sem tipo explicito ou inferido seja tratado como **any**.