---
description: >-
  Olá, Seja bem vinda! Vamos te contar um pouco sobre a Internet e seus
  fundamentos. Por exemplo, sobre o que é a Internet e como funciona?  E também
  um pouco de sua história.
---

# Fundamentos da Internet

### Índice

1. O que é Internet?
2. História da Internet
3. Como a Internet funciona?
4. URL, IP e DNS
5. Caminhos da Internet
6. Rede, Intranet e Extranet
7. IntranetExtranet
8. Navegadores
9. Cliente-Servidor 
10. Referências Bibliográficas 

### O que é Internet?

A internet é um sistema de redes de computadores mundial, todos eles estão ligados uns aos outros. A comunicação via internet pode ser de dados, de voz, vídeo, multimídia, etc.

**Curiosidade:** A palavra internet vem de “inter” que vem de internacional e “net”, que significa rede, ou seja, rede de computadores mundial.

![Fonte: https://www.alainet.org/pt/articulo/190287](https://gblobscdn.gitbook.com/assets%2F-M7-2eRyD9xvpTaq4bz_%2F-M7ebPV4SVquRMyK70Dh%2F-M7ecKjm54l_2jRFapav%2Frede-internet.png?alt=media&token=5d03695e-c04f-4476-aad3-a516d4cc30d5)

### História da Internet

* A internet surgiu a partir de um projeto da agência norte-americana Advanced Research and Projects Agency \(ARPA\), com o objetivo de conectar os computadores de seus departamentos de pesquisa, na década de 1960. Assim surgiu a ARPANET, interligando quatro instituições: a Universidade da California; LA e Santa Bárbara; Instituto de Pesquisa de Stanford e Universidade de Utah.
* Vários estudos e pesquisas se deram a partir deste projeto e, na década de 70, surgiu o TCP/IP \(Transmission Control Protocol/Internet Protocol\), grupo de protocolos que é a base da internet até hoje.
* A entidade americana National Science Foundation \(NSF\) interligou em 1985 os supercomputadores de seu centro de pesquisa, a NSFNET e no ano seguinte entrou para a ARPANET. Essas duas redes passaram a ser a espinha dorsal \(backbone\) de uma nova rede, a INTERNET. **Obs.:** Backbone são a “internet em si”, sem eles a internet não consegue realizar seu trabalho. Alguns dos principais Backbones do Brasil: Oi, Telefônica, Embratel, Comsat Brasil, entre outros.
* Na década de 1990, a internet deixa de ser uma instituição de natureza acadêmica e passa a ser explorada comercialmente, tanto para a construção de novos backbones por empresas privadas quanto para fornecimento de serviços diversos.

### Como a Internet funciona?

Para encontrar e explorar páginas na internet, utiliza-se um navegador de Internet. Navegador é um tipo de software que permite acesso à internet. Basta inserir um endereço Web no navegador para ser levado a este Website.

Para a internet funcionar é preciso dois componentes principais: hardware e protocolos.

* **Hardware** - São os elementos que formam as conexões. Alguns são as pontas finais, como o computador. Outras são desde cabos até o dispositivo usado para acessar a internet como roteadores, servidores, torres de telefonia celular, satélites, entre outros.
* **Protocolos** - Conjunto de regras que as máquinas adotam para completar tarefas. São os protocolos que fornecem o método e a linguagem comum que as máquinas usam para transmitir dados. Existem vários protocolos na internet. Por exemplo, http - usado para ver sites no navegador, aparece na frente de qualquer endereço web. Outro exemplo é o protocolo de controle de transmissão \(TCP\) e protocolo de internet \(IP\), o TCP/IP, que basicamente estabelecem regras de como a informação passa pela internet. Sem isso, o usuário precisaria de conexões diretas para outros computadores para acessar a informação que eles guardam.
  * Os sites se comunicam usando pacotes, que são pequenas quantidades de informação.
  * Cada pacote viaja para a internet e para o computador que o solicitou.
  * Quando o servidor do site que se deseja acessar já se comunicou com o da companhia da internet utilizada, a página vai sendo carregada no computador, dependendo da velocidade contratada.

### **URL, IP e DNS**

* **URL**

  É o endereço Web que é informado em um navegador para chegar a um Website.

  Todos os Websites possuem uma URL, e por sua vez cada URL tem um endereço IP.

  Ex: A URL [_www.gooogle.com_](http://www.gooogle.com) leva ao Website do Google.

* **Endereço IP**

  É uma série de números que indica ao computador onde encontrar as informações que se procura.

  Por serem números longos e complexos, criou-se os URLs, e ao invés de informar um endereço IP para ir para um Website, basta inserir a URL.

  Cada dispositivo \(computador, celular, tablet\) usado para conectar a internet possui um IP único.

  A internet possui inúmeros Websites e endereços IP, mas o navegador não sabe automaticamente a localização de cada um deles. Para procurar cada um deles existe o DNS \(Domain Name System ou Sistema de Nomes de Domínio\).

* **DNS**

  É o tradutor de uma URL, como por exemplo [_www.google.com_](http://www.google.com), em um endereço IP, levando ao Website que se procura, ou seja, o DNS vai apontar a requisição para a direção certa.

  Sem o IP é impossível navegar na internet. Quando se acessa informação de outro computador, os protocolos TCP/IP tornam esta transmissão possível.

  A requisição viaja pela internet e atinge os servidores DNS para encontrar o servidor-alvo.

  É preciso ter uma coordenação global para que o sistema de endereços IP e DNS funcione corretamente, ou seja, para que em qualquer lugar do mundo, para se abrir o site do google, por exemplo, basta digitar [_www.google.com_](http://www.google.com).

  
  **Obs.:**

  ICANN é o nome da organização responsável por atribuir nomes de domínios e endereços IPs em escala mundial.

![Fonte da imagem: iStock \[5\]](https://gblobscdn.gitbook.com/assets%2F-M7-2eRyD9xvpTaq4bz_%2F-M7srUN4ZITMFJzfDT8R%2F-M7srqmnOu5-nhzgmPGF%2Fdns.jpg?alt=media&token=3a3b30b2-ef07-40e5-89b6-ab5aec0d52bd)

### Caminhos da Internet

Os dados enviados pelos usuários são transportados pelo provedor de serviço, então são enviados para o provedor de acesso e chegam novamente ao backbone \(que é uma rede principal por onde os dados dos clientes da internet trafegam\). A partir do backbone, o processo segue o mesmo caminho inicial até o próximo destino. 

**O que acontece quando fazemos uma requisição?**   
Para ter uma idéia do que acontece, veja o exemplo a seguir: 

**=&gt; Qual o primeiro passo?**   
Para acessar uma página online, é preciso abrir o navegador e se conectar ao website que o contém. Ao fazer isso, o computador envia uma requisição eletrônica pela conexão de internet para o provedor de acesso. Este provedor roteia o pedido para um servidor adiante na cadeia da internet. 

**=&gt; O que acontece com essa requisição?**   
Esse pedido vai atingir um DNS \(servidor de nome de domínio\). Esse servidor vai então procurar por um nome de domínio que corresponda com o nome de domínio que a pessoa digitou no campo de endereço do navegador \(ex.: [_www.google.com_](http://www.google.com)\). Se ele encontrar a correspondência, ele vai redirecionar o pedido ao endereço IP apropriado do servidor.   
Se não encontrar, ele irá enviar o pedido a um nível mais alto da cadeia para um servidor que tenha mais informação. Ao achar o servidor requisitado, ele vai responder enviando o arquivo requisitado em uma série de pacotes. Quando os pacotes chegam até o computador que o requisitou, o dispositivo \(computador usado, por exemplo\) os arranja de acordo com as regras dos protocolos.   
É como colocar juntas peças de um quebra-cabeças, e como resultado final, a pessoa vê a página com seu conteúdo.

![O caminho que a informa&#xE7;&#xE3;o percorre at&#xE9; chegar ao seu computador. Fonte: \[4\]](https://gblobscdn.gitbook.com/assets%2F-M7-2eRyD9xvpTaq4bz_%2F-M7spwECn0qSdli3hxi1%2F-M7sqBRneFHGAAnDz-03%2Fcaminhointernet.jpg?alt=media&token=dd2afd3a-4723-46eb-a6e6-d9842f5a2a3f)

### Rede, Intranet e Extranet

**Rede**

Rede de computadores pode ser definida como um conjunto computadores e outros dispositivos interligados entre si de modo a poderem compartilhar recursos, estes podem ser do tipo: dados, impressoras, disco rígido, etc. **Obs.:** A internet, por exemplo, é um sistema que conecta muitas redes de computadores. Existem muitas formas e recursos de vários equipamentos que podem ser interligados e compartilhados, mediante meios de acesso, protocolos e requisitos de segurança. A rede permite a troca de dados entre computadores e a partilha de recursos de hardware e software.

**Tipos de rede:**   
=&gt; **LAN \(Local Area Network\):** são redes locais porque cobrem uma área limitada, visto que quanto maior a distância, maior a taxa de erros que pode ocorrer devido à falha de sinal. São usadas para ligar estações de trabalho, servidores, periféricos, em uma casa, escritório, etc.   
=&gt; **WAN \(Wide Area Network\):** a WAN abrange uma grande área geográfica, como um país ou continente. A internet é a maior WAN que existe. Em geral uma WAN contém um conjunto de servidores que formam sub redes e ligam redes dentro de uma vasta área, permitindo a comunicação a grande distância.

**Intranet** A intranet permite tudo o que a internet dispõe, porém é restrita a um certo público, por exemplo, todos os funcionários de uma empresa podem acessar a intranet com um nome de usuário e senha devidamente especificados pela coordenação da empresa O acesso a intranet geralmente é feito em um servidor local em uma rede local \(LAN\).

**Extranet** Quando alguma informação ou dado da intranet é aberta a clientes ou fornecedores de uma empresa, a rede passa a ser chamada de extranet. ou quando uma empresa tem uma intranet e seu fornecedor também, e ambas essas redes privadas compartilham uma rede entre si \(para facilitar pedidos, pagamentos, etc.\), essa rede compartilhada também é uma extranet. **=&gt;** A diferença básica entre intranet e extranet está em quem gerencia a rede. O funcionamento e a arquitetura da rede é a mesma. Quem gerencia uma intranet é só uma empresa. Já uma extranet, os gerentes são as várias empresas que compartilham a rede.

![Imagem Rede de computadores. Fonte:https://www.tecmundo.com.br/ \[7\]](https://gblobscdn.gitbook.com/assets%2F-M7-2eRyD9xvpTaq4bz_%2F-M7t0BTHjyrLP3wgpG57%2F-M7t3JYdZeSyUWg5N3Uv%2Frede-internet.jpg?alt=media&token=3a3ca4f3-54e5-468e-a2b0-5d0d30a6c9f5)

###  Navegador

O navegador \(ou browser\) é um programa que permite visualizar o conteúdo da rede em sua forma gráfica ao invés de códigos HTML \(linguagem usada para montar o site\).

### **Cliente-servidor**

Como a Internet se tornou uma rede cada vez maior de computadores interligados, houve necessidade de dedicar alguns computadores para prover serviços à rede. Os computadores que proveem serviços são chamados de **Servidores**, e os que acessam e consomem os serviços são chamados de **clientes.**

### Referências Bibliográficas:

\[1\] [https://www.alainet.org/pt/articulo/190287](https://www.alainet.org/pt/articulo/190287)   
\[2\] [https://www.researchgate.net/figure/Hardware-and-software-organization-of-an-Internet-application\_fig1\_2319107](https://www.researchgate.net/figure/Hardware-and-software-organization-of-an-Internet-application_fig1_2319107)   
\[3\] [http://cursocertificado.com.br/os-conceitos-basicos-da-internet/](http://cursocertificado.com.br/os-conceitos-basicos-da-internet/)   
\[4\] [https://www.techtudo.com.br/noticias/noticia/2011/07/como-internet-chega-na-sua-casa.html](https://www.techtudo.com.br/noticias/noticia/2011/07/como-internet-chega-na-sua-casa.html)   
\[5\] [https://www.tecmundo.com.br/o-que-e/829-o-que-e-dns-.htm](https://www.tecmundo.com.br/o-que-e/829-o-que-e-dns-.htm)   
\[6\] [http://todostutoriaisweb.blogspot.com/2013/04/redes-de-computadores-qestionario.html](http://todostutoriaisweb.blogspot.com/2013/04/redes-de-computadores-qestionario.html)   
\[7\] [https://www.tecmundo.com.br/internet/982-o-que-e-cliente-servidor-.htm](https://www.tecmundo.com.br/internet/982-o-que-e-cliente-servidor-.htm)

