# Casos colocados a Testes

<h3>1. Fazer login no app</h3>

   **Criterio de Aceitação:**
  - Temos que ter o acesso a tela de login pela tela inicial, e clicar em "login".  
  - Colocar os dados como nome e senha de sua conta já cadastrados anteriormente.
  - Clicar em "Log In", e esperar ser direcionado a tela inicial novamente com o Login feito.

<h3>2. Mudar a senha de login</h3>

   **Criterio de Aceitação:**
  - Voltar a tela de Login, e clicar na opção "Forgot Password?"  .
  - Informar as informações que forem pedidas na tela para resetar a senha da sua conta direcionada com seu Email ou Nome de usuario.
<h3>3. Criar nova conta</h3>

   **Criterio de Aceitação:** 
  - Na tela de inicial, clicar em "Create New Accont".
  - Informar: Nome, Emial, Senha e Data de Nascimento (Nessa ordem) e por último clicar em Sign up.
  - Deve se ter feito Login automaticamente e enviado a tela inicial.

## Testes de Casos  
  
 1. **Fazer Login:** 
   - Se informarmos dados de um Cadastro inexistente não é feito o Login(Aviso de conta inexistente).
   - Se digitarmos dados de forma incorreta não é feito o Login(Aviso de Senha(ou usuario)incorreto).
   - A caso de senha incorreta, o sistema destaca o botão de "Esqueceu sua senha?".

 2. **Mudar a senha**
   - Se informar um Email para Troca de senha seja o Email de uma conta não cadastrada, informa "Email não associado".
   - Se colocarmos uma senha igual a senha interior, informa que "A senha não pode ser igual a anterior".
   - Se colocarmos um Email invalido (escrito sem o @ ou com algum erro de digitação após o @), é informado que o Email é invalido.

 3. **Criar conta**
   - Se colocarmos a Data de nascimento de forma impossível(30/30/2030) apresenta um aviso de data invalida
   - Se colocarmos Nome de usuario igual a um existente é apresentado um aviso de nome de usuario em uso  
   - Se colocarmos uma senha que não tenha os requisitos minimos de segurança é apresentado uma lista com os requisitos que ainda precisam ser incluidos na senha

 ## Bug encontrado  

   - Se colocarmos um Email já associado a uma conta ele continua o cadastro normalmente, assim criando duas conta com o mesmo Email associados, o que deveria aparecer que o Email já esta associado a outra conta, podendo criar a lacuna de outro usuario alternar os dados de um Email que já está associado a um usuario, trazendo problemas na hora de troca de senha e problemas de comunicação com o Email.  
    Precisamos resolver esse erro antes que o app seja lançado para n termos que resolver com Emails de usuarios já existentes, trazendo problemas aos usuarios que tiveram o Email em duas contas diferentes.

   ### Ideias de Resolução do Bug
     1. Podemos fazer uma parte do sistema para verificar no banco de dados se o Email informado já foi usado em outra conta
     pois não se pode alternar dados de um usuario que não seja o seu.

     2. Se colocarmos a opção de Cadastro com o número de telefone junto com o Email.

     3. Um Email Próprio ao App, de forma que usaria o nome do Usuario para essa Seleção de Email
    com a opção interna na conta uma associação ao Email principal.
      

  

