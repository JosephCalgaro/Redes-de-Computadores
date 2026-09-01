# 01/09
- camadas divididas em protocolos que as "gerem"
- **camada FISICA recebe dados do meio e envia dados da camada de enlace**
- **camada de enlace recebe os dados da camada fisica e fica responsavel por dividir, enquadras, checkar, corrigir e enviar os dados da camada fisica para a camada de rede**
- **A camada de rede é responvavel por "mandar" os dados da origem para o destino atravez do ip**
- endereço ip representa "quem" é a minha rede e "quem" sou eu
- Mascara de rede é um numero que varia entre 0 a 255, determina quantos ips posso utilizar para host

# 18/03
- camada de enlaçe divide os bits em quadros (Enquadramento)
- **Checksum** é um método utilizado para detectar erros ou corrupção de dados durante a transmissão.
- O remetente calcula um valor (checksum) a partir dos dados e o envia junto com a mensagem.
- O receptor realiza o mesmo cálculo e compara os resultados.
- Se os valores forem diferentes, indica que os dados podem ter sido alterados ou corrompidos.
- O checksum detecta erros, mas não necessariamente consegue corrigi-los.
- Contagem de caracteres não é confiavel devido a interferencia
- **Bytes de flag com inserção de bytes**
  - O byte de flag é utilizado para indicar o início e o fim de um quadro.
  - Problema: o byte de flag pode aparecer dentro dos dados.
  - Para evitar que o receptor interprete esse byte como delimitador, utiliza-se um byte de escape (ESC).
  - Quando o byte de flag aparece nos dados, o remetente insere um ESC antes dele.
  - O receptor identifica o ESC e sabe que o flag seguinte faz parte dos dados, removendo o ESC posteriormente.
- **Bytes de Flag com inserção de bits**
  - Utiliza um byte de flag para indicar o início e o fim de um quadro.
  - Para evitar que a sequência do flag apareça dentro dos dados, utiliza-se a inserção de bits (bit stuffing).
  - Sempre que aparecem cinco bits 1 consecutivos nos dados, o transmissor insere automaticamente um bit 0.
  - O receptor remove esse bit 0 após receber os dados.
  - Dessa forma, a sequência de flag não é confundida com parte dos dados.

## Diferença entre Serviço e Protocolo

- **Serviço** → o que é oferecido ao usuário ou a outra aplicação.
- **Protocolo** → as regras de como essa comunicação acontece.

---

## CAMADA FISICA

- Comunicação sem fio modulada atravez de ondas eletromagneticas (comprimento, frequencia e amplitude)
- Velocidade afetada pelo meio
- frequencia alta é absorvida mais facilmente por materiais, pode causar problemas á saúde e são dificeis de serem lidas preciamente, ja ondas de frequencia menor permeam o meio com mais facilidade
- **Espectro de Dispersão por Salto de Frequencia** (método de transmissão de sinais de rádio que altera rapidamente a frequência portadora em uma sequência pseudoaleatória)
- **Espectro de Dispersão de Sequencia Direta** (técnica de modulação em telecomunicações que espalha a energia de um sinal de dados por uma faixa de frequência muito mais ampla, usando códigos pseudoaleatórios)
- **banda ultralarga** (tecnologia de rádio sem fio de curto alcance que transmite dados por meio de pulsos curtos de nanossegundos em uma faixa de frequência superior a 500 MHz)
- **analise de fourier** (serve para dividir qualquer sinal ou função complexa em uma soma de ondas simples, como senos e cossenos)

---

# 11/08

## Modelo OSI Simplificado

**( Fisica, Enlace, Rede, Transporte e Aplicação)**

- Camada Fisica responsavel por transmitir bits
- Meios de transmissão guiados (fios fisicos)
- Vantagens em Frequencia, largura de banda, atraso, custo, facilidade
- Cabos de pares trancçados transmitem dados atravez da diferencia de potencial entre os campos
- podem transmitira dados atravez do meio analógico ou digital
- Protocolos ditam a velocidade que cabos trancados se comunicam, **802.3a -> 100MB/s (fullduplex) | 802.3ab -> 1gb/s (half-duplex)0**
- **Fibra Óptica** superior devido a diversos fatores
