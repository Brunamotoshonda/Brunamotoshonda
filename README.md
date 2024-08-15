document.getElementById("form").addEventListener("submit", function(event) {
    event.preventDefault();

    const cpf = document.getElementById("cpf").value;
    const rg = document.getElementById("rg").value;
    const dataExp = document.getElementById("data-exp").value;
    const estadoCivil = document.getElementById("estado-civil").value;
    const comprovante = document.getElementById("comprovante").files.length;

    if (cpf && rg && dataExp && estadoCivil && comprovante > 0) {
        // Exibe o link dinâmico após o preenchimento
        const message = document.getElementById("message");
        message.textContent = "Formulário preenchido com sucesso!";
        message.style.color = "green";

        const dynamicLink = document.getElementById("dynamic-link");
        dynamicLink.style.display = "block";
        dynamicLink.href = "https://forms.gle/exemplo12345"; // Insira o link do Google Forms
    } else {
        // Mensagem de erro caso os campos obrigatórios não sejam preenchidos
        const message = document.getElementById("message");
        message.textContent = "Por favor, preencha todos os campos obrigatórios.";
        message.style.color = "red";
    }
});


body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
}

.container {
    background-color: white;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    width: 300px;
}

h1 {
    font-size: 20px;
    margin-bottom: 20px;
    text-align: center;
    color: #da251d; /* Cor vermelha padrão Honda */
}

form {
    display: flex;
    flex-direction: column;
}

label {
    margin-bottom: 5px;
    color: #555555; /* Cor cinza */
}

input, select {
    margin-bottom: 15px;
    padding: 10px;
    border-radius: 5px;
    border: 1px solid #ccc;
}

button {
    padding: 10px;
    background-color: #da251d; /* Botão vermelho Honda */
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

button:hover {
    background-color: #bf1f1a; /* Vermelho mais escuro no hover */
}

#dynamic-link {
    display: block;
    text-align: center;
    margin-top: 20px;
    color: #007bff;
}
