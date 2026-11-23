# Fontes e créditos dos dados

## GeoNames

Os arquivos `data/AR.json`, `data/CL.json` e `data/UY.json` contêm índices transformados dos arquivos de códigos postais do [GeoNames](https://www.geonames.org/), licenciados sob [Creative Commons Attribution 3.0](https://creativecommons.org/licenses/by/3.0/).

Transformações: agrupamento por código, seleção de localidade/província/código da província, remoção de duplicatas e ordenação. Não incluímos coordenadas. O arquivo argentino recebe também o complemento de CABA descrito abaixo.

- [Download e documentação dos arquivos](https://www.geonames.org/export/zip/).
- [Licença, esquema e limites da fonte](https://www.geonames.org/export/zip/readme.txt).
- A cobertura chilena é parcial. A consulta usa apenas os três primeiros dígitos e informa a aproximação ao usuário.
- Os registros são fornecidos conforme publicados, sem certificação de atualização ou completude.

## Buenos Aires Data

Crédito: **Gobierno de la Ciudad Autónoma de Buenos Aires / Buenos Aires Data, Ente de Turismo**. Conjunto [Oferta de establecimientos gastronómicos](https://data.buenosaires.gob.ar/dataset/oferta-establecimientos-gastronomicos), sob [CC BY 2.5 Argentina](https://creativecommons.org/licenses/by/2.5/ar/).

Usamos somente a associação dos quatro dígitos numéricos dos CPAs com a cidade de Buenos Aires. Não distribuímos nomes, contatos ou endereços dos estabelecimentos, nem inferimos uma rua ou bairro do hóspede a partir deles. O script de atualização registra a origem exata em `data/metadata.json`.

## Consultas online

- [ViaCEP](https://viacep.com.br/): consulta brasileira por CEP de oito dígitos. Código inexistente e indisponibilidade de rede são tratados separadamente.
- [DINACOPA / Correo Paraguayo](https://codigopostal.paraguay.gov.py/): consulta da zona postal atual. [Descrição oficial do código de seis dígitos](https://correoparaguayo.gov.py/sitio/el-codigo-postal-es-importante-para-ubicar-las-direcciones/).
- [Zippopotam.us](https://www.zippopotam.us/), com dados GeoNames: consultas de Estados Unidos e França. [Cobertura e limitações](https://docs.zippopotam.us/docs/getting-started/).

As respostas online são exibidas durante a consulta, sem criar uma base ou histórico persistente de endereços.

## Referência de formato argentino

O [Correo Argentino](https://www.correoargentino.com.ar/5-sobre-la-informacion-que-brinda-correo-oficial) informa que o CPA é o formato vigente e que o código antigo de quatro dígitos não recebe manutenção oficial. Esta extensão mantém o formato antigo como consulta de localidade para atendimento e sinaliza essa limitação.
