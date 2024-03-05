# Casos colocados a Testes

<h3>1. Fazer login no app</h3>

   **Criterio de Aceitação:**
  - Na tela Inicial precisamos de um botão "login" que leve a tela de Login.   
  - A tela de Login deve ter as opções para colocar o nome de usuário e a opção de colocar a senha.
  - Validar se os dados informados são parte de uma conta já criada
  - Se for bem sucessido, abrir a tela inicial com a conta do login colocado
  - Se tiver dados errados, mostrar uma mensagem de erro na tela

<h3>2. Mudar a senha de login</h3>

   **Criterio de Aceitação:**
  - Na tela de Login deve ter o campo de "Esqueci minha senha".
  - Ao clique do Campo "Esqueci minha senha", Deve pedir um Email para a redefinação.
  - No Email a ser recebido deve conter a opção de redefinição de senha.
  - Ao clique redefinição de senha deve aparecer para o usuário mobile campos para informar a nova senha e um botão de concluído.
  - Caso colocar senha igual a antiga, informar em tela
  - Após a redefinição deve se estar na tela de Login novamente.
<h3>3. Criar nova conta</h3>

   **Criterio de Aceitação:** 
  - Na tela inicial do App deve conter um botão de Criar nova conta que leve para a Página de Cadastro
  - A tela de Cadastro deve conter as opções de informar o Email, Senha, Nome e Data de nascimento, com um botão de Fazer Cadastro
  - Após conclução na tela de cadastro deve se abrir na tela inicial, cadastrado na conta criada.

## Casos de teste
  
 1. **Fazer Login:** 
   - Apertar em Login na tela inicial
   - Quando na tela de Login informar o Nome e Senha da conta do usuário
   - Após informar, clicar em Log-In 

 **Resposta esperada:** Um login na conta do usuário será feito e abrirá a tela inicial com o login feito

 2. **Mudar a senha**
   - Na tela de login, clicar em 'Esqueci a minha senha'
   - Informar o Email da conta que gostaria de trocar a senha
   - Abrir o Email recebido e clicar na opção de troca de senha
   - Passar a nova senha a ser usada para acessar a conta do Email e clicar em "Mudar minha senha"
   - Voltar ao app e ir na tela de Login.

 **Resposta esperada:** Que a senha do usuário será trocada com sucesso e o Login será feito com a nova senha   
 3. **Criar conta**
   - Clicar em "Cadastrar-se" na tela inicial
   - Na tela de cadastro, informar o Nome, Email, Senha e Data de nascimento 
   - Clicar em Cadastrar

 **Resposta esperada:** Criará uma conta para o usuário com os dados informados na tela de cadastro   

## Bug encontrado  
 1. **tentar acessar com Email já cadastrado**
    - Clicar em "Cadastra-se"
    - Informar os dados de nome, senha e data de nascimento normalmente, mas o campo de Email informar um Email já cadastrado
    - Clicar em Cadastrar

  **Resposta esperada:** Informará erro de Impossibilidade de criação de conta por dados iguais

  **Resposta encontrada:** Uma nova conta de usuário é criada com o Email igual a o de outra conta de usuário   
       


   ### Ideias de Resolução do Bug
     1. Podemos fazer uma parte do sistema para verificar no banco de dados se o Email informado já foi usado em outra conta
     pois não se pode alternar dados de um usuario que não seja o seu.

     2. Se colocarmos a opção de Cadastro com o número de telefone junto com o Email, mesmo que seja
     colocado um email igual, a gente impossibilitando o login por números iguais, deixaria as duas contas com 
     email igual, mas com associações de números de contatos diferente. 

     3. Um Email Próprio ao App, de forma que usaria o nome do Usuario para essa Seleção de Email
    com a opção interna na conta uma associação ao Email principal, tendo alguns riscos mais depende
    da finalidade que o App deseja.
      

  

