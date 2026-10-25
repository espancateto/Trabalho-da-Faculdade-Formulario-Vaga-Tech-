# Trabalho-da-Faculdade-Formulario-Vaga-Tech-
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Vaga Tech | Criar conta</title>

    <link rel="stylesheet" href="style.css">
</head>
<body>

    <main class="container">

        <header class="logo">
            <div class="logo-icon">
               <img src="logo VagaTech.ico" alt="Logo VagaTech">
    </div>
            </div>
            <h1>Vaga<span>Tech</span></h1>
        </header>

        <section class="cadastro">
            <div class="cabecalho">
                <span class="etiqueta">COMECE SUA JORNADA</span>
                <h2>Crie sua conta</h2>
                <p>
                    Cadastre-se para encontrar vagas mais rapidas nos lugares que utilizem nossos sensores 
                </p>
            </div>

            <form id="formCadastro">

                <div class="campo">
                    <label for="nome">Nome</label>
                    <input
                        type="text"
                        id="nome"
                        name="nome"
                        placeholder="Digite seu nome"
                        autocomplete="given-name"
                        required
                    >
                </div>

                <div class="campo">
                    <label for="sobrenome">Sobrenome</label>
                    <input
                        type="text"
                        id="sobrenome"
                        name="sobrenome"
                        placeholder="Digite seu sobrenome"
                        autocomplete="family-name"
                        required
                    >
                </div>

                <div class="campo">
                    <label for="email">E-mail</label>
                    <input
                        type="email"
                        id="email"
                        name="email"
                        placeholder="seuemail@exemplo.com"
                        autocomplete="email"
                        required
                    >
                </div>

                <div class="campo">
                    <label for="senha">Senha</label>
                    <input
                        type="password"
                        id="senha"
                        name="senha"
                        placeholder="Mínimo de 8 caracteres"
                        minlength="8"
                        autocomplete="new-password"
                        required
                    >
                </div>

                <div class="campo">
                    <label for="confirmarSenha">
                        Confirmar senha
                    </label>
                    <input
                        type="password"
                        id="confirmarSenha"
                        name="confirmarSenha"
                        placeholder="Digite a senha novamente"
                        minlength="8"
                        autocomplete="new-password"
                        required
                    >
                </div>

                <button type="submit" class="botao">
                    Criar minha conta
                    <span aria-hidden="true">&rarr;</span>
                </button>

                <p id="mensagem" class="mensagem" role="status"></p>

            </form>

            <p class="login">
                Já tem uma conta?
                <a href="#">Faça login</a>
            </p>
        </section>

        <footer>
            VAGA TECH &bull; VAGAS INTELIGENTES 
        </footer>
    </main>

    <script>
        const formulario = document.getElementById("formCadastro");
        const senha = document.getElementById("senha");
        const confirmarSenha = document.getElementById("confirmarSenha");
        const mensagem = document.getElementById("mensagem");

        formulario.addEventListener("submit", function(event) {
            event.preventDefault();

            if (senha.value !== confirmarSenha.value) {
                mensagem.textContent = "As senhas não são iguais.";
                mensagem.className = "mensagem erro";
                confirmarSenha.focus();
                return;
            }

            mensagem.textContent =
                "Validação concluída! O próximo passo é integrar o cadastro ao servidor.";
            mensagem.className = "mensagem sucesso";
        });
    </script>

</body>
</html>
