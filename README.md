# Estudo_De_Caso_Sistema_Imobiliaria 👨‍💻

Sistema de geração de orçamentos de locação

Início do desenvolvimento da aplicação responsável pela geração de orçamentos de locação da R.M.

Nesta primeira versão, foi estruturado o fluxo principal da aplicação, incluindo a seleção do tipo de imóvel, aplicação dos valores e regras de locação, cálculo de adicionais como quartos e garagem, descontos quando aplicáveis e inclusão da taxa de contrato imobiliário.

A aplicação também contempla a organização dos dados do orçamento e a geração das informações necessárias para o período de locação, mantendo o fluxo alinhado às regras definidas para o projeto.

Este commit marca a base inicial da aplicação, que será utilizada para as próximas etapas de implementação, validação e aprimoramento do sistema.

⚙️ Como funciona

O sistema começa solicitando o nome do cliente e apresenta os três tipos de locação disponíveis:

🏢 Apartamento — R$ 700,00
🏠 Casa — R$ 900,00
🏙️ Studio — R$ 1.200,00

Depois da escolha do imóvel, o sistema aplica as regras correspondentes à modalidade selecionada.

🏢 Apartamento

Para apartamentos, o sistema verifica se o cliente possui crianças.

Caso o cliente não possua crianças, é aplicado um desconto de 5% no valor do aluguel.

Também é possível adicionar um quarto, com acréscimo de:

🛏️ Quarto adicional — R$ 200,00

A garagem possui acréscimo de:

🚗 Garagem — R$ 300,00
🏠 Casa

Para casas, o valor inicial é de R$ 900,00.

O cliente pode adicionar:

🛏️ Quarto adicional — R$ 250,00
🚗 Garagem — R$ 300,00
🏙️ Studio

Para o Studio, o valor inicial é de R$ 1.200,00.

O sistema permite adicionar estacionamento pelo valor de:

🚗 Garagem/estacionamento — R$ 250,00

Também é possível acrescentar vagas adicionais:

➕ Vaga adicional — R$ 60,00 por vaga
💰 Contrato imobiliário

Além do valor mensal do aluguel, a aplicação considera o contrato imobiliário definido no estudo de caso.

O contrato possui o valor de:

R$ 2.000,00

O cliente pode escolher entre 1 e 5 parcelas.

O sistema calcula automaticamente o valor de cada parcela de acordo com a quantidade escolhida.

ℹ️ O parcelamento do contrato imobiliário é independente das 12 parcelas geradas no arquivo CSV.

📋 Funcionalidades
👤 Cadastro do nome do cliente;
🏢 Seleção do tipo de imóvel;
🔎 Validação das opções de locação;
💰 Cálculo do valor inicial do aluguel;
👶 Aplicação de desconto de 5% para apartamentos sem crianças;
🛏️ Inclusão de quarto adicional;
🚗 Inclusão de garagem;
🅿️ Inclusão de vagas adicionais para Studio;
📄 Cálculo do contrato imobiliário;
💳 Parcelamento do contrato em até 5 vezes;
🖥️ Apresentação do resumo do orçamento no terminal;
📊 Geração do arquivo .csv;
📅 Geração de 12 parcelas do orçamento;
🖥️ Exibição das parcelas no terminal.
📊 Regras de negócio
Item	Valor
🏢 Apartamento	R$ 700,00
🏠 Casa	R$ 900,00
🏙️ Studio	R$ 1.200,00
📄 Contrato imobiliário	R$ 2.000,00
🛏️ Quarto adicional — Apartamento	+ R$ 200,00
🛏️ Quarto adicional — Casa	+ R$ 250,00
🚗 Garagem — Apartamento	+ R$ 300,00
🚗 Garagem — Casa	+ R$ 300,00
🅿️ Garagem — Studio	+ R$ 250,00
➕ Vaga adicional — Studio	+ R$ 60,00
👶 Desconto — Apartamento sem crianças	5%
🚀 Como executar
Pré-requisito

É necessário ter o Python 3 instalado no computador.

A aplicação utiliza apenas recursos da biblioteca padrão do Python, portanto não é necessário instalar bibliotecas externas.

▶️ Executando o projeto

Clone o repositório:

git clone https://github.com/EmersonRicardo2504/Estudo_De_Caso_Sistema_Imobiliaria.git

Entre na pasta:

cd Estudo_De_Caso_Sistema_Imobiliaria

Execute o arquivo Python:

python aplicação.py

💡 Caso o arquivo Python possua outro nome no repositório, utilize o nome correspondente ao arquivo presente no projeto.

Durante a execução, basta seguir as opções apresentadas no terminal.

📁 Geração do arquivo CSV

Ao finalizar o orçamento, a aplicação gera automaticamente o arquivo:

orcamento.csv

O arquivo possui as seguintes informações:

Cliente | Parcela | Valor

São registradas 12 parcelas do orçamento, permitindo que o arquivo seja aberto posteriormente em programas de planilha, como o Microsoft Excel.

Além da criação do arquivo, as parcelas também são exibidas no terminal para facilitar a conferência dos valores.

🛠️ Ferramentas utilizadas
🐍 Python 3 — desenvolvimento da aplicação;
📄 Biblioteca csv — geração do arquivo de orçamento;
🔀 Git — controle de versão;
🐙 GitHub — armazenamento e versionamento do projeto;
📐 PlantUML — elaboração do Diagrama de Atividades UML;
📊 Microsoft Excel — visualização e conferência do arquivo CSV.
📂 Estrutura do projeto
Estudo_De_Caso_Sistema_Imobiliaria/
│
├── aplicação.py
├── UML_atividade.puml
└── README.md

📌 O arquivo orcamento.csv é gerado durante a execução da aplicação e, por isso, não precisa fazer parte da estrutura permanente do projeto.

📄 aplicação.py

Contém a implementação principal do sistema, incluindo as regras de negócio, validações, cálculos, funções de impressão e geração do arquivo CSV.

📐 UML_atividade.puml

Contém o Diagrama de Atividades UML utilizado para representar visualmente o fluxo da aplicação.

📖 README.md

Documento que apresenta o objetivo, funcionamento, regras de negócio, execução e ferramentas utilizadas no projeto.

🎓 Objetivo acadêmico

O projeto foi desenvolvido com finalidade acadêmica para aplicar, na prática, conceitos de programação em Python e desenvolvimento de aplicações.

Durante a implementação foram utilizados conceitos como:

Variáveis;
Estruturas condicionais;
Estruturas de repetição;
Funções;
Validação de entradas;
Operações matemáticas;
Manipulação de arquivos;
Geração de arquivos CSV;
Modelagem por UML;
Controle de versão com Git e GitHub.

O projeto também busca demonstrar a relação entre requisitos, implementação, modelagem e documentação, mantendo o código alinhado ao estudo de caso proposto pela empresa R.M.
