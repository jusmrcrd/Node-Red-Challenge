# Node-Red-Challenge

Este projeto foi desenvolvido como parte de um desafio técnico que envolvia a construção de uma aplicações usando o Node-RED para processamento e manipulação de dados. O objetivo principal era integrar e exibir dados a partir de uma API externa, permitindo a interação dinâmica através de um front-end simples e funcional.


# Tecnologias Utilizadas

    Node-RED: Ferramenta principal para o desenvolvimento de lógica e integração do fluxo.
    BrasilAPI - CEP V2: API pública utilizada para consulta dos dados de CEP.
    BrasilAPI - Corretoras: API pública utilizada para consulta dos dados das corretoras nos arquivos da CVM
    HTML/CSS/JavaScript: Para o frontend e manipulação de elementos.

# Requisitos

Para rodar este projeto, você precisará dos seguintes softwares instalados:

    Node.js (versão 14 ou superior)
    Node-RED
    Docker (opcional, para execução simplificada com Docker)
    

# Executando Localmente


Com o Node.js e npm instalados, você pode instalar o Node-RED globalmente usando o npm:

    sudo npm install -g --unsafe-perm node-red

Para rodar a aplicação localmente, basta executar o comando abaixo:

    node-red


Em seguida, abra o Node-RED no navegador:

    http://localhost:1880





# Executando com Docker (Opcional)

Com o docker instalado Execute o contêiner:

    docker run -p 1880:1880 -v node_red_data:/data --name node-red-container node-red-desafio

Acesse o Node-RED no navegador: 

     http://localhost:1880


Endpoints da API

O projeto inclui os seguintes endpoints configurados no Node-RED para lidar com a funcionalidade de busca e exibição de CEP e lista de Catalogo de corretoras:

    GET /zip_searcher/:zip 
        Descrição: Este endpoint recebe um parâmetro cep e retorna os detalhes do CEP buscado, como estado, cidade, bairro e rua.
        Exemplo de Uso: http://localhost:1880/zip_searcher/47645-970    
   
    GET /broker_catalog
        Descrição: Este endpoint lista a lista de corretoras nos arquivos da CVM
        Exemplo de Uso: http://localhost:1880/broker_catalog
