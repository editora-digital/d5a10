---
layout: post
title: "Feliz Dia Nacional do Livro Infantil"
description: "Para comemorar, preparamos um presente especial
 para você enviar a quem quiser!"
permalink: /DNLI5/feliz-dia-nacional-livro-infantil
author: Parau
categories: [DNLI5]
image: assets/images/posts2020/dnli5/feliz-dia-nacional-livro-infantil.jpg
tags: [Literatura]
---

<style>
.onomegente {float: right; width: 45%;}
.amazon {float: right; width: 25%; margin-left: 10px; margin-top: 10px; box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);}
.bruxa {float: right; width: 25%;}
.kindle {float: right; width: 35%; padding:10px;}
.d5a10 {
  font-family: 'Crafty Girls', cursive;
  color:gray;
  font-weight: bold;
}
figure {
  margin: 0rem;
}
figcaption {
display: block;
position: relative;
top:-30px;
font-style: italic;
text-align: center;
}
@media (min-width: 576px) {
  .bd-example {
      position: relative;
      padding: 1.5rem;
      /*margin-right: 0;
      margin-left: 0;*/
      border-width: .2rem;
      /*border: solid #f7f7f9;*/
      background-color: #e8f3ec;
  }
}
@media (max-width: 575px) {
  .bd-example {
      position: relative;
      padding: 0.5rem;
      /*margin-right: 0;
      margin-left: 0;*/
      background-color: #e8f3ec;
  }
}
.loading{
  background-image : url('/assets/images/loading02.gif');  
  background-repeat:no-repeat;
  background-size: contain;
}
.center {
  /*display: block;
  margin-left: auto;
  margin-right: auto;*/
  width: 40px;
  margin-bottom: 0;
}
</style>
Neste dia 18 de abril é **Dia Nacional do Livro Infantil** e aniversário do escritor Monteiro Lobato. E nós só poderíamos comemorar essa data de um jeito muito especial: incentivando a leitura! Por isso, junto com a equipe APRENDER.digital, preparamos uma versão online do livro **O NOME DA GENTE**, com acesso livre, para você personalizar e enviar de presente para aquela criança que você quer bem! (Ah, pode ser adulto também!!! 😉).

Para enviar o livro digital de presente é muito simples. Basta preencher o formulário nesta página 👇 e clicar para gerar o livro.

Ao final da versão digital, você encontra a informação de como enviar o *link* para quem deseja. Você pode copiar o *link* ou enviar pelo whatsapp!

**O NOME DA GENTE** é um livro exclusivo e personalizável, que traz a criança como um personagem da história, no qual ela reconhece o seu nome escrito, as letras, os sons, a similaridade com outras palavras. Além disso, propõe a participação da família no processo de alfabetização e no estímulo da criança à leitura.

Qualquer dúvida ou comentário deixe a sua [mensagem aqui](https://www.facebook.com/d5a10/posts/154273796121337){:target="_blank"}!!!

Gostou? Vamos gerar seu exemplar do livro?! 🎁

<div class="bd-example" style="font-family:'Segoe UI', 'Helvetica Neue', 'Arial'">
      <form id="formLivro" name="formLivro" target="_blank" class="needs-validation" novalidate action="https://livros.aprender.digital/DNLI5/ONomeDaGente.html#book/page/1" method="GET">
        <div class="form-group">
          <label for="de"><b>Seu nome</b></label>
          <input type="de" class="form-control form-control-lg" placeholder="Digite aqui o seu nome" maxlength="25" required
              id="formde" name="de">
          <div class="invalid-feedback">
            🙄 Escreva aqui o seu nome.
          </div>
          <small id="nomeProfHelp" class="form-text text-muted">
            Você pode usar até 25 letras. Se não couber, use alguma abreviação. Por exemplo: Prof. Ana Julia.
          </small>
        </div>
        <div class="form-group">
          <label for="nome">
            <b>Nome criança</b>
          </label>
          <input type="nome" class="form-control form-control-lg" placeholder="Digite aqui o nome da criança" maxlength="15" required id="formNome" name="nome" onkeyup="DefineNome(this)">
          <div class="invalid-feedback">
              🙄 Escreva aqui o nome da criança que vai receber o livro.
          </div>
          <small id="nomeHelp" class="form-text text-muted">
            Aqui você você escreve o nome da criança que vai receber o livro. 
            Use no m&aacute;ximo 15 letras.
            Sugerimos usar o nome sem o sobrenome. Por exemplo: Julia, Ana Cl&aacute;udia, Felipe.
          </small>
        </div>
        <div class="form-group">
          <label for="frase"><b>Escolha a frase abaixo de acordo com a criança que vai receber o livro</b></label>
          <div class="custom-control custom-radio form-control-lg">
            <input type="radio" class="custom-control-input" id="dele" name="deleDela" value="dele" required>
            <label id="deleLabel" class="custom-control-label" for="dele">
              O nome <b>dele</b> é...</label>
          </div>
          <div class="custom-control custom-radio form-control-lg">
            <input type="radio" class="custom-control-input" id="dela" name="deleDela" value="dela" required>
            <label id="delaLabel" class="custom-control-label" for="dela">
              O nome <b>dela</b> é...</label>
              <div class="invalid-feedback">
                👆 Não deixe de escolher uma das frases acima.
              </div>
          </div>
        </div>
        <br />
        <button name="enviar" style="display: none;" type="submit"></button>
        <button id="botaoGerarLivro" type="button" onclick="callGerar()" class="heart btn btn-success btn-block mt-2">Clique aqui para <b>GERAR O LIVRO</b></button>
      </form>
</div>
<script>
  function DefineNome(input) {
      document.getElementById("deleLabel").innerHTML = "O nome <b>dele</b> é " + input.value + ".";
      document.getElementById("delaLabel").innerHTML = "O nome <b>dela</b> é " + input.value + ".";
  }
  (function() {
    'use strict';
    window.addEventListener('load', function() {
      // Fetch all the forms we want to apply custom Bootstrap validation styles to
      var forms = document.getElementsByClassName('needs-validation');
      // Loop over them and prevent submission
      var validation = Array.prototype.filter.call(forms, function(form) {
        form.addEventListener('submit', function(event) {
          if (form.checkValidity() === false) {
            event.preventDefault();
            event.stopPropagation();
          }
          else {
            //alert("navegar");
            //event.preventDefault();
            //event.stopPropagation();
            //window.location.href = 'livro-gerar.html';
          }
          form.classList.add('was-validated');
        }, false);
      });
    }, false);
  })();

  function callGerar() {
   if (document.formLivro.checkValidity()) {
     document.getElementById("botaoGerarLivro").disabled = true;
     document.getElementById("botaoGerarLivro").innerHTML = 'Gerando o livro... <img class="center" src="/assets/images/loading03.gif"> Uma nova janela será aberta!';
     setTimeout(callSubmit, 4000);
   } else {
     document.formLivro.enviar.click();
   }
  }
  function callSubmit() {
     document.getElementById("botaoGerarLivro").disabled = false;
     document.getElementById("botaoGerarLivro").innerHTML = 'Clique aqui para <b>GERAR O LIVRO</b>';
    document.formLivro.enviar.click();
  }
</script>


<small><i>Este texto foi produzido em parceria com o 5ª edição projeto [Dia Nacional do Livro Infantil](https://dnli.aprender.digital){:target="\_blank"} **#DNLI5**</i></small>
