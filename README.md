📝 **README - Criando um formulário para salvar dados de usuário em SQLite usando o WPF no Visual Studio Code (VS Code)** 🖥️

Para criar um formulário para salvar dados de usuário em SQLite usando o WPF no Visual Studio Code (VS Code), você precisará seguir alguns passos:

1️⃣ **Configure o projeto WPF:**
   - Siga os passos que mencionei anteriormente para criar um novo projeto WPF no VS Code.

2️⃣ **Adicione a referência ao SQLite:**
   - No seu projeto WPF, você precisará adicionar uma referência ao pacote NuGet do SQLite. Abra um terminal no VS Code, navegue até o diretório do projeto e execute o comando `dotnet add package Microsoft.EntityFrameworkCore.Sqlite` para adicionar o pacote SQLite ao seu projeto.

3️⃣ **Modele a classe de usuário:**
   - Crie uma classe para representar os dados do usuário. Por exemplo, você pode ter uma classe chamada "User" com propriedades como "Id", "Nome", "Email" etc.

4️⃣ **Crie o banco de dados e a tabela:**
   - Você precisará criar um banco de dados SQLite e uma tabela para armazenar os dados do usuário. Isso pode ser feito no código C#. Você pode usar a biblioteca Entity Framework Core para simplificar essa tarefa. Defina uma classe de contexto que herde de `DbContext` e configure uma propriedade DbSet para representar a tabela de usuários.

5️⃣ **Crie a interface gráfica do formulário:**
   - No XAML do seu projeto WPF, crie uma interface gráfica para o formulário onde o usuário pode inserir os dados, como caixas de texto para nome, email etc., e um botão para salvar os dados.

6️⃣ **Manipule o evento do botão salvar:**
   - No código C#, associe o evento do botão salvar ao método que será executado quando o usuário clicar no botão. Dentro desse método, você precisará recuperar os dados inseridos pelo usuário, criar uma instância da classe "User" com esses dados e salvar no banco de dados.

7️⃣ **Use o SQLite para salvar os dados:**
   - No método de salvamento, use o contexto do Entity Framework Core para inserir os dados do usuário na tabela do SQLite.

🔍 Esses são os passos básicos para criar um formulário para salvar dados de usuário em SQLite usando o WPF no VS Code. Lembre-se de que você precisará ter algum conhecimento de programação em C#, XAML e SQLite para implementar essas etapas com sucesso. 🚀

🌐 **Referências:**
- Documentação oficial do Microsoft Entity Framework Core: [https://docs.microsoft.com/ef/core/](https://docs.microsoft.com/ef/core/)
- Documentação oficial do SQLite: [https://www.sqlite.org/docs.html](https://www.sqlite.org/docs.html)
- Documentação oficial do WPF (Windows Presentation Foundation): [https://docs.microsoft.com/en-us/dotnet/desktop/wpf/?view=net-desktop-5.0](https://docs.microsoft.com/en-us/dotnet/desktop/wpf/?view=net-desktop-5.0)

🔗 **Repositório do projeto:**
- [wpf-raiz-vscode](https://github.com/seu-usuario/wpf-raiz-vscode)
