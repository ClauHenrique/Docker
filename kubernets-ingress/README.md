# descrição
Nesses dois arquivos estamos criando uma estrutura separada em dois hambientes. São dois namespaces diferentes:
  - develop
  - homolog
Criamos Um Deployment para levantar nossos pods, definindo a quantidade de replicas para 2.
Cada Deployment é executado em um ambiente diferente - namespace.
Alem do Deployment, criamos um Ingress para que os ambientes possam ser acessados por meio de uma url.
São dois tipos de Ingress diferentes. Um cria uma rota para o ambiente de develop e o outro para o ambiente de homolog

# Estrutura dos arquivos
Normalmente seria necessário criar manifestes diferentes para cada tipo de serviço:
  - namespace.yml
  - deployment.yml
  - services.yml
  - ingress.yml

Mas nos exemplos desse repositorio estamos criando toda essa estrutura dentro de apenas um arquivo .yml
É possivel fazer isso separadom seus serviços por ---
"  criar namespace
    suas configurações

  ---

  criar deployment
    suas configurações

  ---

  criar service
    suas configurações

  ---
criar ingress
  suas configurações
"
