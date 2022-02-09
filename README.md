# Primeiro-Formulario
Criação do primeiro formulário em HTML/CSS

Em html:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
<link rel= "stylesheet" type="text/css" href="formulario.css" media ="screen"
    <title>Cadastro</title>
</head>
<body>

    <div>
         <h1 id="titulo">Cadastro de DEVs</h1>
         <p id="subtitulo">Complete suas informações</p>
         <br>
    </div>

    <form>
         <fieldset class="grupo">
             <div>
                 <label for="name"><strong>Nome</strong></label>
                 <input type="text" name="nome" id="nome" required>
             </div>

             <div class="campo"> 
                 <label for="Sobrenome"><strong>Sobrenome</strong></label>
                 <input type="text" name="sobrenome" id="sobrenome" required>
             </div>
         </fieldset>

         <div class="campo">
             <label for="email"><strog>Email</strog></label>
             <input type="email" name="email" id="email" required>
         </div>
       

         <div class="campo">
           <label>De qual lado da aplicação você desenvolve?</label>
           <label>
               <input type="radio" name="devweb" value="frontend" checked>Front-end      
           </label>
            <label>
               <input type="radio" name="devweb" value="backend">Back-End 
               
            </label>
            <label>
                <input type="radio" name="devweb" value="fullstack">Fullstack 
            </label>
         </div>


         <div class="campo">
             <label for="senioridade"><strong>Senioridade</strong></label>
             <select id="senioridade">
                 <option selected disabled value="">Selecione</option>
                 <option>Junior</option>
                 <option>Pleno</option>
                 <option>Senior</option>
             </select>
         </div>
         <fieldset class="grupo">
             <div id="check">
                 <label><strog>Selecione as tecnologias que utiliza:</strog></label><br><br>
                 <input type="checkbox" id="tecnologia1" name="tecnologia1" value="HTML">
                 <label for="tecnologia1">HTML</label>
                 <input type="checkbox" id="tecnologia2" name="tecnologia2" value="CSS">
                 <label for="tecnologia2">CSS</label>
                <input type="checkbox" id="tecnologia3" name="tecnologia3" value="Javascript">
                <label for="tecnologia3">Javascript</label>
            
             </div>
         </fieldset>
         <div class="campo">
             <br>
             <label>Conte um pouco sobre da sua experiência</label>
             <textarea row="6" style="width: 26em" id="experiência" name="experiencia"></textarea>
         </div>

         <button class="botão" type="submit">Concluido</button>
    </form>
    
</body>
</html>



em css:

*{
    margin: 0;
    padding: 0;
    
}
#titulo {
    font-family: sans-serif;
    color: #380b38;
    margin-left: 7%;   
}

#subtitulo{
    font-family: sans-serif;
    color: #380b38;
    margin-left: 10%;   
}

fieldset{
    border:0;
}

body{
    background-color: #F0F8FF;
    font-family: sans-serif;
    font-size: 1em;
    color: #59429d;
    margin-left: 36%;
    margin-top: 2%;
    justify-content: center;
}

input, select, textarea, button{
    border-radius: 5px;

}
.campo{
    margin-bottom: 1em;
}

.campo label {
    margin-bottom: 0.2em;
    color: #59429d;
    display: block;
}

fieldset.grupo .campo{
    float: left;
    margin-right:1em;
}

.campo input[type="text"], .campo input [type="email"], .campo select, .campo textarea{
    padding: 0.2em;
    border: 1px solid #59429d;
    box-shadow: 2px 2px 2px rgba(0,0,0,0.2);
    display: block;

}

.campo select option{
    padding-right: 1em;
}

.campo input:focus, .campo select:focus, .campo textarea:focus{
    background: #E0E0F8;
}

.botão {
    font-size: 1.2em;
    background: #59429d;
    border: 0;
    margin-bottom: 1em;
    color: #ffff;
    padding: 0.2em 0.6em;
    box-shadow: 2px 2px 2px rgba(0,0,0,0.2);
    text-shadow: 1px 1px 1px rgba(0,0,0,0.5);
    position: absolute;
    top:90%;
    left:50%;
    margin-left: -50%;
    transform: translate(-50%, -50%);
}

.botão:hover{
    background: #ccbbff;
    box-shadow: inset 2px 2px 2px rgba(0,0,0,0.2);
    text-shadow: none;
}
.botão,select{
    cursos: pointer;
}
#check {
    display: inline-block;
}
