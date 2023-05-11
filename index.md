# **Criando uma documentação em MarkDown com ReadTheDocs**

#### **OBS: Certifique-se que o pip está instalado no seu ambiente**

## Configurando ReadTheDocs + MarkDown

### **1°** Instale o sphinx 
  **``pip install sphinx``**

### **2°** Crie um diretório para a documentação e execute o sphinx

**``cd “diretório-criado” && sphinx-quickstart``**

### **3°** Siga o seguinte passo a passo para configuração do seu diretório

- **\> Separar os diretórios de origem e compilação (y/n) \[n\]: n**

- **\> Nome do projeto: “Nome do seu projeto”**

- **\> Nome(s) de autor(es): “Seu nome”**

- **\> Lançamento do projeto \[\]: “Versão do projeto”**

- **\> Idioma do projeto \[en\]: pt_BR**

### **4°** Abra o arquivo “conf.py” 

**``nano conf.py``**

### **5°** Configure da seguinte maneira para leitura de documentações em .md

**\# -- General configuration
---------------------------------------------------**

**extensions = \["myst_parser"\]**

**templates_path = \['\_templates'\]**

**exclude_patterns = \['\_build', 'Thumbs.db', '.DS_Store'\]**

**language = 'pt_BR'**

**\# -- Options for HTML output
-------------------------------------------------**

**html_theme = 'sphinx_rtd_theme'**

**html_static_path = \['\_static'\]**

### **6°** Mude o nome do arquivo “index.rst” para “index.md” e altere seu conteudo

**``mv index.rst index.md && nano index.md``**

- **Exemplo de estrutura em MarkDown**

**\# Título Principal**

**Este é um exemplo de texto em \*\*Markdown\*\*. Ele permite que você
formate o texto de maneira simples e rápida.**

**\## Título Secundário**

**\### Listas**

**Você pode criar listas usando os símbolos de hífen (-) ou asterisco
(\*). Por exemplo:**

**- Item 1**

**- Item 2**

**- Item 3**

**\### Ênfase**

**Você pode adicionar ênfase ao texto usando asteriscos ou sublinhados.
Por exemplo:**

**- \*Itálico\***

**- \*\*Negrito\*\***

**- \~~Riscado\~~**

**\### Links**

**Você pode criar links usando a seguinte sintaxe:**

**\[Texto do Link\](https://www.exemplo.com)**

**\### Código**

**Você pode destacar trechos de código usando crases (\`) ou criar
blocos de código usando três crases. Por exemplo:**

**``print("Olá, mundo!")``**

### **7°** Crie a página em HTML da sua documentação

**``make html``**

### **8°** Você pode acessar o html criado no seu navegador com esse comando

**``xdg-open /caminho/para/o/arquivo.html``**

Fazendo o deploy da sua documentação no ReadTheDocs

**OBS: Você deve fazer um commit do diretório do projeto que foi criado
com sphinx para o github**

### **1°** Acesse o ReadTheDocs no navegador:

**http://\<IP-da-máquina\>:8001**

### **2°** Faça login como admin

- **usuário: admin**

- **senha: admin**

### **3°** Clique em “admin” e depois clique em “importar projeto”

### **4°** Clique em “importar manualmente” e siga esses passos

**Nome: \<Nome do projeto\>**

**URL do Repositório: \<url do repositório github\>**

**Tipo de Repositório: Git**

- **Edite as opções avançadas do projeto: Sim**

**OBS: Caso queira um repositório com tudo configurado, você pode clonar
o repositório abaixo**

[**<u>https://github.com/EduardoVasconceloss/Markdown-Docs-With-ReadTheDocs.git</u>**](https://github.com/EduardoVasconceloss/Markdown-Docs-With-ReadTheDocs.git)

### **5°** Continue a importação seguindo esses passos

**Description: \#Opcional**

**Tipo Documentação: \<Sphinx Html\>**

**Idioma: \<Portuguese\>**

**Linguagem de Programação : \<Only Words\>**

**Tags: \#Opcional**

**Página do Projeto: \#Opcional**

### **6°** Clique em finalizado e espere, provavelmente você terá um erro devido a branch escolhida pelo ReadTheDocs, mude as configurações

- **Clique em “Admin”**

- **Clique em “Config Avançadas”**

- **Branch padrão: \<main\>**

- **Arquivos Requerimentos: \<requirements.txt\>**

- **Agora clique em “Salvar”**

### **7°** Veja sua documentação clicando em “Visualizar Documentação”

### 

### 

### 
