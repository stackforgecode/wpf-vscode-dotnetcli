# Como criar um formulário com entrada de dados com WinForms usando Visual Studio Code :computer:

Neste tutorial detalhado, vamos explorar passo a passo como criar um formulário com entrada de dados utilizando o Windows Forms (WinForms) no Visual Studio Code. O WinForms é uma tecnologia da Microsoft que permite criar interfaces gráficas para aplicações desktop usando a linguagem C#.

## Descrição

O Windows Forms é uma opção popular para desenvolver interfaces de usuário no ecossistema .NET. Com o Visual Studio Code, uma poderosa ferramenta de desenvolvimento multiplataforma, você pode criar formulários com entrada de dados de forma simples e eficiente.

## 1. Configuração do ambiente de desenvolvimento

Antes de começarmos, é necessário configurar o ambiente de desenvolvimento. Certifique-se de ter o seguinte instalado em seu sistema:

- [.NET SDK](https://dotnet.microsoft.com/download) - Baixe e instale a versão mais recente do .NET SDK adequada ao seu sistema operacional.

- [Visual Studio Code](https://code.visualstudio.com/) - Faça o download e instale o Visual Studio Code, um editor de código altamente configurável e extensível.

- [C# extension for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp) - Instale a extensão C# para o Visual Studio Code, fornecendo recursos adicionais para desenvolvimento em C#.

## 2. Criação de um novo projeto de formulário do WinForms

Agora, vamos criar um novo projeto do Windows Forms no Visual Studio Code:

1. Abra o Visual Studio Code e clique em "File" (Arquivo) na barra de menu superior.
2. Selecione "Open Folder" (Abrir Pasta) e escolha um diretório para o seu projeto.
3. Abra o terminal integrado do Visual Studio Code clicando em "View" (Exibir) na barra de menu superior e, em seguida, "Terminal" (Terminal).
4. No terminal, digite o seguinte comando para criar um novo projeto WinForms:
```shell
dotnet new winforms
```
5. Aguarde até que o comando seja concluído e o projeto seja criado.

## 3. Adição de controles de entrada de dados ao formulário

Agora que temos um novo projeto do WinForms, vamos adicionar controles de entrada de dados ao formulário:

1. No Visual Studio Code, navegue até a pasta do projeto que foi criada.
2. Abra o arquivo "Form1.cs" no diretório "Form1".
3. No método `InitializeComponent()`, você pode adicionar controles como TextBoxes, Labels e Buttons ao formulário.
   - Por exemplo, para adicionar uma caixa de texto e um botão, insira o seguinte código no método `InitializeComponent()`:

```csharp
private void InitializeComponent()
{
    // ...
    // Código existente

    TextBox textBox = new TextBox();
    Button button = new Button();

    textBox.Location = new Point(50, 50);
    button.Location = new Point(50, 80);

    textBox.Name = "txtInput";
    button.Name = "btnSubmit";

    button.Text = "Enviar";
    button.Click += BtnSubmit_Click;

    Controls.Add(textBox);
    Controls.Add(button);

    // ...
    // Código existente
}
```

## 4. Manipulação dos dados inseridos pelo usuário

Agora que adicionamos os cont

roles de entrada de dados ao formulário, vamos manipular os dados inseridos pelo usuário:

1. No mesmo arquivo "Form1.cs", adicione o seguinte código para manipular o evento de clique do botão "Enviar":

```csharp
private void BtnSubmit_Click(object sender, EventArgs e)
{
    TextBox textBox = Controls.Find("txtInput", true).FirstOrDefault() as TextBox;

    if (textBox != null)
    {
        string inputText = textBox.Text;
        MessageBox.Show("Você inseriu: " + inputText);
    }
}
```

Neste código, encontramos a TextBox pelo seu nome "txtInput" e obtemos o texto inserido pelo usuário. Em seguida, exibimos uma caixa de diálogo com a mensagem contendo o texto inserido.

## 5. Compilação e execução do projeto

Agora que o formulário com entrada de dados está pronto, vamos compilá-lo e executá-lo:

1. No terminal integrado do Visual Studio Code, navegue até a pasta raiz do projeto.
2. Execute o seguinte comando para compilar o projeto:
```shell
dotnet build
```
3. Após a compilação bem-sucedida, execute o seguinte comando para executar o projeto:
```shell
dotnet run
```
4. O formulário com entrada de dados será exibido e você poderá testar o campo de entrada e o botão de envio.

## Referências

Aqui estão algumas referências úteis para aprender mais sobre o desenvolvimento de formulários com WinForms no Visual Studio Code:

- [Documentação oficial do Windows Forms](https://docs.microsoft.com/pt-br/dotnet/desktop/winforms/?view=net-desktop-6.0)
- [Tutorial de introdução ao Windows Forms no Visual Studio Code](https://docs.microsoft.com/pt-br/dotnet/desktop/winforms/get-started/?view=net-desktop-6.0&tabs=vscode)
- [Guia completo do Visual Studio Code para C# e .NET](https://code.visualstudio.com/docs/languages/csharp)

Agora você está pronto para criar seus próprios formulários com entrada de dados utilizando o WinForms no Visual Studio Code. Divirta-se codificando! 💻🔥
