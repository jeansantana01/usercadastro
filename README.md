<?php session_start() ?>
<!DOCTYPE html>

<html>
    <head>
        <meta charset="UTF-8">
        <!--Import Google Icon Font-->
        <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
           <!--Import materialize.css-->
        <link rel="stylesheet" href="materialize/css/materialize.min.css">
    
        <title></title>
    </head>
    <body>
        
        <nav class="blue-grey">
            <div class="nav-wrapper container">
                <div class="brand-logo light">Sistema de Cadastro</div>
                <ul class="right">
                    <li><a href=""><i class="material-icons left">account_circle</i>Cadastro</a></li>
                    <li><a href=""><i class="material-icons left">search</i> Consultas</a></li>
            
                </ul>
            </div>
        </nav>   
        
        <!--Formulário de Cadastro-->
        
        <div class="row container">
            <p>&nbsp;</p>
            <form action="banco_de_dados/create.php" method="post" class="col s12">
                <fieldset class="formulario">
                    <legend><img src="imagens/avatar.png" alt"[imagem]" width="100"></legend>
                    <h5 class="light center">Cadastro de Clientes</h5>
                    
                    <?php
                        if(isset($_SESSION['msg'])):
                            echo $_SESSION['msg'];
                            session_unset();
                        endif;
                    ?>
                  
                    
                    <!--CAMPO NOME-->
                    
                    <div class="input-field col s12">
                         <i class="material-icons prefix">account_circle</i>
                        <input type="text" name="nome" id="nome" maxlength="40" required autofocus>
                        <label for="nome">Nome do Cliente</label>
                        
                        
                    </div>
                    
                    <!-- CAMPO EMAIL-->

                    <div class="input-field col s12">
                        <i class="material-icons prefix">email</i>
                        <input type="email" name="email" id="email" maxlength="50" required>
                        <label for="email">Email do Cliente</label>
                
                    </div>
                    
                     <!-- CAMPO TELEFONE-->
                     <div class="input-field col s12">
                        <i class="material-icons prefix">phone</i>
                        <input type="tel" name="telefone" id="telefone" maxlength="15" required>
                        <label for="telefone">Telefone do Cliente</label>
                
                    </div>
                    
                    <!--BOTÕES-->
                    <div class="input-field col s12">
                        <input type="submit" value="cadastrar" class="btn blue">
                        <input type="reset" value="limpar" class="btn red">
                    </div>
                    
                </fieldset>
            </form>
        </div>
        
            
        <!--Arquivos Jquery e Javascript-->
        <script type="text/javascript" src="materialize/js/jquery-3.4.1.min.js"></script>
        <script type="text/javascript" src="materialize/js/materialize.min.js"></script>
        
        <!--Inicialização Jquary -->
        
        <script type="text/javascript">
            $(document).ready(function() {
                
            });
        
        </script>
      

    </body>


</html
