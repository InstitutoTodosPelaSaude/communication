# Comunicação: Conversão de Documentos Word/Docs para HTML

Este projeto foi criado para automatizar a conversão de textos em Word ou Google Docs para HTML usando R. Ele facilita a replicação de conteúdos em um formato web, mantendo a qualidade e a organização do conteúdo, especialmente para fins de publicação.

## Por que?

A necessidade de converter documentos de texto ricos em formatação, como os criados no Word ou Google Docs, para HTML de maneira eficiente e consistente é essencial para manter a integridade do conteúdo ao ser publicado online. Este projeto visa simplificar esse processo, evitando a perda de formatação e facilitando o gerenciamento de imagens e estilos.

## O que?

Este projeto utiliza R e Quarto para realizar a conversão de documentos de texto para HTML, mantendo o controle sobre o formato, imagens, e estilos CSS. As principais funcionalidades incluem:

- **Conversão de documentos**: Automatiza a conversão de arquivos `.docx` para HTML.
- **Gerenciamento de imagens**: Garante que as imagens sejam armazenadas corretamente e referenciadas dentro do HTML.
- **Customização de estilos**: Permite personalizar os estilos CSS para atender às necessidades específicas de cada publicação.

## Como?

### 1. Configuração do Ambiente

Para começar, você precisa ter R e Quarto instalados. Se ainda não tiver, siga os passos abaixo:

```bash
# Instalar Quarto
install.packages("quarto")

# Instalar pacotes necessários no R
install.packages(c("rmarkdown", "knitr", "fs", "stringr"))
```

### 2. Estrutura de Pastas

Cada notícia ou artigo deve ter sua própria pasta, organizada da seguinte forma:

```
noticia/
│
├── noticia.qmd
├── img/
│   └── suas-imagens.png
└── styles/
    └── custom.css
```

- **`noticia.qmd`**: O arquivo principal em Quarto Markdown onde o conteúdo da notícia é estruturado.
- **`img/`**: Todas as imagens relacionadas à notícia devem ser armazenadas nesta pasta. Certifique-se de referenciar corretamente as imagens no `noticia.qmd`.
- **`styles/`**: Personalize o CSS criando um arquivo `custom.css` nesta pasta para ajustar o estilo conforme necessário.

### 3. Boas Práticas para Imagens

- **Organização**: Sempre crie uma pasta `img` dentro da pasta da notícia para armazenar todas as imagens.
- **Referência**: No arquivo `.qmd`, referencie as imagens usando o caminho relativo, por exemplo, `![Alt text](img/suas-imagens.png)`.
- **Tamanho e Proporção**: Redimensione as imagens de forma apropriada para manter a qualidade e o tempo de carregamento ideal.

### 4. Personalização de Estilos

- **Edição de Estilos**: Modifique o CSS diretamente no arquivo `custom.css` dentro da pasta `styles` para ajustar a aparência do HTML gerado.
- **Manutenção de Consistência**: Garanta que as alterações no CSS sejam consistentes com o layout geral do site ou publicação para manter uma identidade visual coesa.

### 5. Executando o Projeto

Para gerar o HTML, navegue até a pasta da notícia e execute:

```bash
quarto render index.qmd
```

Isso criará um arquivo `noticia.html` na mesma pasta, pronto para ser publicado.

### Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests com melhorias e correções.

---

Este projeto facilita a criação de conteúdo web de alta qualidade a partir de documentos de texto, mantendo a integridade e o estilo necessários para uma presença online profissional.

Para mais informações, consulte a documentação do [Quarto](https://quarto.org/).
