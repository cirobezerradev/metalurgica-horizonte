Briefing da Empresa: Metalúrgica Horizonte Ltda.
Nota: Esta é uma empresa fictícia criada para fins de desenvolvimento web.

1. Dados Oficiais
Item	Dados
Nome	Metalúrgica Horizonte Ltda. (empresa fictícia)
Atividade	Usinagem CNC, estamparia, solda robotizada e tratamento superficial
Fundação	1998 (28 anos de atuação)
Equipe	120 colaboradores, três turnos
Mercados	Automotivo, agrícola e fabricantes de máquinas
Diferenciais	Qualidade rastreável por lote • prazo combinado • segurança e manutenção preventiva
Serviços	Usinagem CNC (tolerâncias de até 0,01 mm) • Estamparia (prensas de 60 a 250 t) • Solda robotizada MIG/MAG • Pintura eletrostática a pó e zincagem
Capacidade por turno	Usinagem: 400 peças (12 tornos e 8 centros) • Estamparia: 500 peças (10 prensas) • Solda: 180 conjuntos (3 células) • Pintura: 300 peças (1 linha)
Contato	Rua das Indústrias, 1000 • Distrito Industrial • Cidade Exemplo – SP • (11) 00000-0000 • contato@metalurgicahorizonte.example
Horário	Segunda a sexta, das 7h às 17h
Identidade Visual	Azul #3776AB • Amarelo #FFD43B • Azul-escuro #1F2937 • Cinza-claro #F3F4F6
2. Requisitos do Projeto (Estrutura Mínima)
Abaixo estão os requisitos obrigatórios para a construção do site, conforme a Figura 2.

#	Requisito
R1	Pelo menos 3 páginas: index.html (Início), servicos.html (Serviços) e contato.html (Contato)
R2	Menu igual em todas as páginas, com links relativos (href="servicos.html") e destaque para a página atual
R3	Estrutura semântica: <header>, <nav>, <main>, <footer>; um único <h1> por página
R4	lang="pt-BR", meta viewport, title e meta description próprios em cada página
R5	Um único arquivo styles.css, usando as cores da identidade visual
R6	Layout responsivo: legível no computador e no celular
R7	Início: chamada principal, números da empresa e diferenciais
R8	Serviços: os quatro serviços e uma tabela de capacidade por turno
R9	Contato: endereço, telefone, e-mail (mailto:), horário e perguntas frequentes
R10	Imagens com alt; nomes de arquivos em minúsculas e sem espaços
R11	Rodapé informando que a empresa é fictícia
R12	[NOVO] Criar um ícone/logo em formato SVG para a marca da empresa, transmitindo a ideia de uma metalúrgica moderna e industrial, utilizando as cores da identidade visual.
3. Sugestão de Estrutura de Arquivos
Para organizar o projeto, sugere-se a seguinte estrutura de pastas:

text
/
├── index.html
├── servicos.html
├── contato.html
├── css/
│   └── styles.css
├── img/
│   ├── logo.svg          <-- (Requisito R12)
│   ├── usinagem.jpg
│   ├── estamparia.jpg
│   ├── solda.jpg
│   └── pintura.jpg
└── README.md
4. Ideia para o Ícone SVG (Requisito R12)
Para representar uma metalúrgica industrial moderna, o ícone SVG pode combinar:

Formas geométricas (engrenagens estilizadas, linhas de precisão).

Cores: Fundo ou traços em Azul Escuro (#1F2937), detalhes em Azul (#3776AB) e um toque de Amarelo (#FFD43B) para representar energia/faísca ou o metal aquecido.

Sugestão de desenho: Um "H" estilizado (de Horizonte) formado por duas barras de aço (azul escuro) e um círculo central (amarelo) que lembra uma engrenagem ou um sol nascente (horizonte).

Exemplo de código SVG minimalista para servir de base:

xml
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" width="100" height="100">
  <!-- Círculo externo (Engrenagem/Industrial) -->
  <circle cx="50" cy="50" r="45" fill="#1F2937" />
  <!-- Letra H estilizada (Horizonte) -->
  <rect x="25" y="25" width="10" height="50" fill="#3776AB" />
  <rect x="65" y="25" width="10" height="50" fill="#3776AB" />
  <rect x="35" y="45" width="30" height="10" fill="#FFD43B" />
  <!-- Detalhe de faísca/brilho -->
  <circle cx="50" cy="50" r="5" fill="#F3F4F6" />
</svg>
