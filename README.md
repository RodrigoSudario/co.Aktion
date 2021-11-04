
<h2>- O que vocês farão? </h2>
  O Squad decidiu criar uma conta Google para a empresa Só Sabão. Com a conta será feito um cadastro no EmailJS, um serviço de captação de emails.
<h2>- Qual o processo?</h2>
  Faremos uma landing page com React e nele será utilizado o framework EmailJS para identificar nos campos do formulário da página informações como Nome, Email e mensagem. 
<h2>- Como farão?</h2

Como no exemplo na documentação:
https://www.emailjs.com/docs/examples/reactjs/

Instalar as dependências e importar:</br>
import emailjs from 'emailjs-com';

Depois será necessário utilizar e emailjs de forma correta utilizando os id’s informados no cadastro no site Emailjs, exemplo:


  const sendEmail = (e) => {
  
    e.preventDefault();
    emailjs.sendForm('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', form.current, 'YOUR_USER_ID')
      .then((result) => {
          console.log(result.text);
      }, (error) => {
          console.log(error.text);
      });
 
  };
  
<h2>- Como os dados serão armazenados?</h2>

Os dados serão salvos no próprio banco do EmailJS, mas o squad está procurando uma forma de requisitar todos emails já recebidos e salvar no MongoDB.
