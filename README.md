# Inventário de Jogo — The Legend of Zelda: Tears of the Kingdom

## 1. Introdução

### Objetivo da Atividade

O objetivo deste projeto é desenvolver um sistema de inventário funcional utilizando tecnologias web como HTML, CSS e PHP, baseado no universo do jogo *The Legend of Zelda: Tears of the Kingdom*.

### O que é um inventário em um jogo?

Um inventário é uma funcionalidade comum em jogos eletrônicos que permite ao jogador armazenar, organizar e utilizar itens coletados durante o jogo. Exemplos incluem armas, poções, materiais de construção, alimentos, entre outros. No *Tears of the Kingdom*, por exemplo, o jogador pode coletar espadas, escudos, ingredientes e ferramentas, que ficam organizados em diferentes categorias no inventário.

### Que tipos de sistemas utilizam essa funcionalidade?

Sistemas de inventário são amplamente utilizados em sistemas de empresa com estoque, jogos de aventura, RPGs e jogos de sobrevivência. Exemplos:

- *Minecraft*: itens de construção e criação.
- *Mercado Livre*: aplicativos de venda online em geral que tenah estoque.
- *Skyrim*: inventário com peso limitado que impacta a mobilidade do personagem.

### Por que essa funcionalidade é importante?

O inventário é essencial para a progressão do jogador no jogo. Ele permite o gerenciamento de recursos, estratégias de combate e personalização do personagem, aumentando a imersão e a complexidade da experiência de jogo.

---

## 2. A Implementação

### 🖥️ Front-End

#### 🛠️ Ferramentas Utilizadas

- <img align="center" alt="Theus-HTML" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg">**HTML**: Estruturação do conteúdo da página.
- <img align="center" alt="Theus-CSS" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg">**CSS**: Estilização visual e responsividade.
- **Editor**: *[Seu editor preferido, ex: VS Code]* — utilizado para escrever e organizar o código.

Essas ferramentas foram escolhidas por serem amplamente suportadas e ideais para construção rápida de interfaces web interativas e personalizadas.

#### 🧩 Layout e Interface

A interface foi dividida em setores bem definidos:

- Login e Logout
- Grade de inventário com ícones representando os itens.
- Itens que pode ser cadastrados.

O layout segue uma organização em **linhas e colunas**, semelhante à grade de inventário dos jogos da franquia Zelda, tornando a navegação intuitiva.

---

### 🧠 Back-End

#### 🛠️ Ferramentas Utilizadas

- <img align="center" alt="Theus-PHP" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/php/php-original.svg">**PHP**: Linguagem usada para processar as ações do inventário, como adicionar ou remover itens.
- **Servidor Local (XAMPP/WAMP)**: Utilizado para rodar scripts PHP em ambiente local.

#### Um exemplo do código PHP com a lógica de registrar itens:<br>

```
<?php
        $file = "inventario.txt";

        if (file_exists($file)) {
            $items = file($file, FILE_IGNORE_NEW_LINES | FILE_SKIP_EMPTY_LINES);

            foreach ($items as $item) {
                list($name, $quantity, $url) = explode("|", $item);
                echo "<div class='item'>
                        <img src='$url' alt='$name'>
                        <h3>$name</h3>
                        <p>Qtd: $quantity</p>
                      </div>";
            }
        } else {
            echo "<p>Nenhum item cadastrado ainda.</p>";
        }
        ?>
```
<br>

## Tela de login
![pag-login](https://github.com/user-attachments/assets/766d0959-bd02-435b-b01f-6855bab3eabb)
<br>

### Usuário: User
### Senha: User123

## Página de login incorreto
![pag-login-incorreto](https://github.com/user-attachments/assets/cbb98ae2-09fc-4cea-bb1a-f980918bf23d)
<br>

## Inventário do jogo
![inventario](https://github.com/user-attachments/assets/db602167-aad0-45df-9329-242f7373fe2c)
<br>

## Cadastro de itens
![add-item](https://github.com/user-attachments/assets/2279132a-b6ad-4cf4-869c-d8bf98174f53)
<br>


## 3. Passo a Passo de Execução
### Como executar o projeto
- Faça o download da pasta MatheusINFO3:

- Instale um servidor local como XAMPP ou WAMP.

- Mova a pasta com os arquivos do projeto para a pasta htdocs (no caso do XAMPP). <br>

  <pre><code>C:\xampp\htdocs</code></pre>
  
- Inicie o servidor Apache no painel do XAMPP.

- Acesse o projeto pelo navegador digitando:<br>

  <pre><code>localhost/MatheusINFO3/login.php</code></pre>

## Explicação da hierarquia

### Os arquivos da pasta são esses:
![hierarquia](https://github.com/user-attachments/assets/6312993e-116b-46bc-bc2b-faaae0ba1400)

- A pasta sql 📂, está os arquivos .sql apra conexão com o banco de dados PhpMyAdmin
- O arquivo "login.php", deve ser o primeiro arquivo a ser executado com o seguinte comando em um browser:
  
  <pre><code>localhost/MatheusINFO3/login.php</code></pre>

### Agora, é só divertir! 😊
 
> "Nada é impossível quando se dá o primeiro passo" - Matheus Gonçalves
