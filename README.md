# 1.0
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Site Básico</title>
    <style>
        /* Estilos CSS */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }
        
        body {
            background-color: #f4f4f4;
            color: #333;
            line-height: 1.6;
        }
        
        header {
            background: #35424a;
            color: #fff;
            padding: 20px 0;
            text-align: center;
        }
        
        nav {
            background: #e8491d;
            padding: 10px;
        }
        
        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
        }
        
        nav ul li {
            margin: 0 15px;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
        }
        
        .container {
            width: 80%;
            margin: auto;
            padding: 20px;
        }
        
        .main-content {
            padding: 20px;
            background: white;
            margin-top: 20px;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        
        footer {
            background: #35424a;
            color: white;
            text-align: center;
            padding: 20px;
            margin-top: 20px;
        }
        
        button {
            background: #e8491d;
            color: white;
            border: none;
            padding: 10px 20px;
            margin: 10px 0;
            cursor: pointer;
            border-radius: 5px;
        }
        
        button:hover {
            background: #333;
        }
    </style>
</head>
<body>
    <header>
        <h1>Bem-vindo ao Meu Site</h1>
    </header>
    
    <nav>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">Sobre</a></li>
            <li><a href="#">Serviços</a></li>
            <li><a href="#">Contato</a></li>
        </ul>
    </nav>
    
    <div class="container">
        <section class="main-content">
            <h2>Sobre Nós</h2>
            <p>Este é um site básico criado para demonstrar a estrutura HTML, CSS e JavaScript.</p>
            
            <button id="changeTextBtn">Clique Aqui</button>
            <p id="demoText">Este texto vai mudar quando você clicar no botão.</p>
            
            <h3>Nosso Time</h3>
            <ul id="teamList">
                <li>João - Desenvolvedor</li>
                <li>Maria - Designer</li>
            </ul>
        </section>
    </div>
    
    <footer>
        <p>&copy; 2023 Meu Site Básico. Todos os direitos reservados.</p>
    </footer>
    
    <script>
        // JavaScript para interatividade
        document.getElementById('changeTextBtn').addEventListener('click', function() {
            document.getElementById('demoText').textContent = 'O texto foi alterado com JavaScript!';
            
            // Adicionar novo membro ao time
            const teamList = document.getElementById('teamList');
            const newMember = document.createElement('li');
            newMember.textContent = 'Carlos - Gerente de Projetos';
            teamList.appendChild(newMember);
        });
        
        // Mudar cor de fundo ao passar o mouse no header
        const header = document.querySelector('header');
        header.addEventListener('mouseover', function() {
            this.style.backgroundColor = '#2c3e50';
        });
        
        header.addEventListener('mouseout', function() {
            this.style.backgroundColor = '#35424a';
        });
    </script>
</body>
</html>
