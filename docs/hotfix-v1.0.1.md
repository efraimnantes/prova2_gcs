# Hotfix v1.0.1

## Falha simulada

Após a preparação da versão v1.0, foi identificada uma falha na tela de login do dashboard EduStream.

A falha estava relacionada ao uso de sessionStorage para verificar se o usuário estava autenticado. Em alguns casos, ao abrir a página login.html, o sistema tentava redirecionar para a própria tela de login, causando um comportamento de recarregamento contínuo.

## Impacto

A falha poderia impedir o usuário de acessar corretamente o dashboard, prejudicando o fluxo de autenticação simulado.

## Correção aplicada

A correção removeu a verificação automática de sessão da tela de login e simplificou o fluxo:

1. O usuário informa e-mail e senha.
2. Se os dados forem válidos, o sistema redireciona para edustream_dash2.0.html.
3. Se os dados forem inválidos, uma mensagem de erro é exibida.
4. O botão de logout apenas redireciona o usuário de volta para login.html.

## Resultado

A versão v1.0.1 corrige o problema de redirecionamento e mantém o login simulado funcionando corretamente.
