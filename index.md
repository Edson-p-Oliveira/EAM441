---
  title: |
    Projeto Geométrico de Loteamento no CAD
  author: "Edson Oliveira"
  date: " 23 abril, 2026"
  output: 
      html_document:
          hightlight: textmate
          includes:
            in_header: 'logotipo.html'
          theme: flatly
          number_sections: true 
          fig_caption: true
          keep_md: true
          toc: true 
          toc_float: true
          collapsed: true
          smooth_scroll: true
              
      
---

# Procedimentos

### Comando `UNITS`

Permite definir corretamente as unidades do projeto, configurando o formato e a precisão das medidas lineares e angulares do desenho, garantindo que o software interprete adequadamente os valores inseridos.

### Comando `LA`

Permite acessar o Layer Properties, onde foram adicionado seis layers: Vias, Contornos, Pontos, Cotas,
Textos e ViewPort, cada uma com suas respectivas configurações de Plot, Color, Linetype e Lineweight,
constituindo o Property Filter "Loteamento".

### Configurando Textos e Cotas

#### Textos

Os estilos de texto utilizados foram criados e configurados por meio da janela "Text Style", 
acessada pelo menu Annotate > Text Style > Manage Text Styles.

#### Cotas

Utilizadas nas medidas do projeto basearam-se no modelo ISO-25 e foram personalizadas por meio do 
botão Modify, com ajustes nas guias Lines, Symbols and Arrows, Text, Fit, Primary Units, Alternate 
Units e Tolerances. Ressalta-se que a janela de configuração pode ser acessada em 
Annotate > Dimension Style > Manage Dimension Styles.

### Plotando os pontos especificados

Foi utilizado o comando `PTYPE` para definir o estilo de ponto e, com o layer Pontos ativado, 
o comando `POINT` para inserir as coordenadas abaixo.


<table class="table table-striped table-hover table-responsive" style="width: auto !important; margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:center;"> PONTO </th>
   <th style="text-align:center;"> ABSCISSA (X) </th>
   <th style="text-align:center;"> ORDENADA (Y) </th>
  </tr>
 </thead>
<tbody>
<tr>
   <td style="text-align:center;"> A </td>
   <td style="text-align:center;"> 4878.622 </td>
   <td style="text-align:center;"> 5570.143 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> PT1 </td>
   <td style="text-align:center;"> 4897.804 </td>
   <td style="text-align:center;"> 5581.120 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> B </td>
   <td style="text-align:center;"> 4931.078 </td>
   <td style="text-align:center;"> 5575.776 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> C </td>
   <td style="text-align:center;"> 4974.531 </td>
   <td style="text-align:center;"> 5557.845 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> PT2 </td>
   <td style="text-align:center;"> 4989.542 </td>
   <td style="text-align:center;"> 5545.343 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> D </td>
   <td style="text-align:center;"> 4990.488 </td>
   <td style="text-align:center;"> 5525.098 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> E </td>
   <td style="text-align:center;"> 5000.000 </td>
   <td style="text-align:center;"> 5500.000 </td>
  </tr>
</tbody>
</table>

### Delineando os contornos da via através da faixa central

Os segmentos entre os pontos foram conectados por meio do comando `LINE` e, nos trechos curvos, 
pelo comando `FILLET`. Em seguida, as linhas foram unificadas com o comando `JOIN` e aplicaram-se
afastamentos de 3 unidades e 1 unidade por meio do comando `OFFSET`, definindo os limites da via 
e da calçada. A faixa central foi ajustada pelo menu Properties, utilizando o comando `LTS` para 
definir o padrão de tracejado.

### Delimitações dos contornos dos lotes

Na maioria dos lotes, utilizou-se a interseção de círculos para determinar os vértices faltantes, 
sempre aplicando os filtros do OSNAP para conectar os segmentos aos nós e às interseções corretas.

# Outras renderizações {.tabset .tabset-fade}

## Plotagem (2D)

<a href="https://drive.google.com/file/d/1HolEoJ3SZlhlSynMjhwUaCcv_U2B7KAa/view?usp=drive_link">
<img src="https://github.com/Edson-p-Oliveira/CloudFiles/blob/main/Imagens/Plotagem.png?raw=true" alt="Texto Alternativo" style="width:70%; height:auto;">
</a>
<br>
<a href="https://drive.google.com/file/d/1HolEoJ3SZlhlSynMjhwUaCcv_U2B7KAa/view?usp=drive_link" download="NomeDoArquivo.pdf">Clique aqui para baixar o PDF</a>

## Modelagem (Revit)

<img src="https://raw.githubusercontent.com/Edson-p-Oliveira/CloudFiles/298644c6b4da70b45547acb0c86f01b7834a03ab/Imagens/loteamento_v2.png" alt="Texto Alternativo" style="width:75%; height:auto;">
