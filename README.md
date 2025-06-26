# os-mecanica-modelo-conceitual

<h1>🛠️Sistema de Gestão de Ordem de Serviço para Oficina Mecânica:</h1>
Este projeto apresenta a modelagem conceitual de um banco de dados relacional, que representa o núcleo de um sistema de gestão para oficinas mecânicas.
O objetivo é estruturar de forma eficiente e escalável o controle de ordens de serviço, clientes, veículos, peças, serviços e equipes de mecânicos.

<h1>🎯Propósito</h1>
<h4>O sistema visa oferecer um controle completo do fluxo de trabalho da oficina, permitindo:</h4>
<ul>
  <li>Cadastro de clientes e seus respectivos veículos.</li>
  <li>Registro detalhado de cada serviço executado, incluindo valor de mão de obra e descrição.</li>
  <li>Controle de peças utilizadas em cada reparo, com quantidade e valores.</li>
  <li>Atribuição de equipes de mecânicos responsáveis por cada OS.</li>
  <li>Acompanhamento do status das ordens de serviço (aguardando, em andamento, concluída etc).</li>
</ul>

<h1>⚙️Diagrama de Entidade-Relacionamento (ERD)</h1>
<p><img src="https://github.com/marcelo-carv/os-mecanica-modelo-conceitual/blob/main/OS_mecanico_1.png"></p>

<h1>🧩 Estrutura Lógica do Modelo</h1>
A estrutura do banco de dados foi pensada para refletir de forma fiel o dia a dia de uma oficina mecânica, usando os princípios dos bancos relacionais e boas práticas de modelagem. A ideia é conectar todas as informações de forma lógica, coerente e eficiente.
<h4>Veja como as partes se encaixam:</h4>

<ul>
  <li>Clientes e Veículos:
Cada cliente pode ter um ou mais veículos cadastrados. Esse vínculo é importante para rastrear todo o histórico de serviços realizados por veículo e por cliente.</li>
  <li>Ordens de Serviço (OS):
São o centro de tudo. Cada OS está ligada a um veículo e a uma equipe, e nela ficam registradas todas as ações realizadas: os serviços executados, as peças utilizadas, os valores cobrados e as datas de emissão e entrega. É o documento que resume todo o atendimento.</li>
  <li>Serviços e Peças:
Os serviços contam com uma descrição e o valor da mão de obra. As peças, por sua vez, têm valor unitário. Ambos são relacionados a cada OS por meio de tabelas intermediárias, o que permite saber exatamente quais e quantos serviços e peças foram aplicados em cada atendimento, facilitando o cálculo do custo total.</li>
  <li>Equipes e Mecânicos:
Uma OS é atribuída a uma equipe responsável. E cada equipe pode ter vários mecânicos, que podem também participar de outras equipes, conforme a necessidade da oficina. Esse formato garante flexibilidade e organização na alocação da mão de obra.</li>
</ul>

<h1>📄 O Que Você Vai Encontrar no Esquema?</h1>
<h4>O diagrama conceitual detalha:</h4>

<ul>
  <li>As entidades principais (Cliente, Veículo, Ordem de Serviço, Mecânico, Equipe, Peça, Serviço).</li>
  <li>Seus atributos essenciais (nome, placa, valor, data, status, etc).</li>
  <li>Os relacionamentos entre entidades, com cardinalidades e chaves primárias/estrangeiras.</li>
  <li>O uso de tabelas associativas para modelar relacionamentos muitos-para-muitos de forma eficiente.</li>
</ul>




