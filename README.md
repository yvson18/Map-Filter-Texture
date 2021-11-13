<h1 align = "center"> Atividade Prática 4 - Mapeamento e Filtragem de Texturas </h1>

<h3 align="center"> João Victor Rodrigues Galvão - 20190172620</h3>
<h3 align="center"> Yvson Nunes Figueiredo - 20190019716</h3>

## Introdução
O Trabalho desenvolvido aqui teve como objetivo realizar uma comparação entre os filtros de texturas estudados em sala e as suas respectivas utilidades em situações de magnificação e minificação. Para Tal, os filtros oferecidos pela biblioteca do threeJS (**NearestFilter**, **LinearFilter**, **NearestMipmapNearestFilter**, **NearestMipmapLinearFilter**, **NearestFilter**, **LinearMipmapNearestFilter** e **LinearMipmapLinearFilter**) foram utilizados.

<h2>Fenômeno de Magnificação</h2>

Em primeiro plano, para a análise da Magnificação, foi utilizada uma imagem de dimensões 125x107 **texels**.  A figura 1 ilustra um cubo o qual foi aplicado o filtro **Nearest neighbor** e, por tal razão, temos um resultado bastante pixelado, fruto da magnificação causada pela baixa resolução.

<h3 align = "center">Nearest neighbor</h3>

<br>
<p align = "center">
<img  style = "justify-content: center" src= "prints/akuaku_pixelado.png" alt =   "drawing" width = "306" height = "298">
</p>
<p align = "center">
<b> Figura 1: Aku Aku (Game: Crash Bandicoot)  - magFilter: NearestFilter</b><p>
</p>

Por outro lado, A figura 2 ilustra o mesmo cubo com a filtragem sendo a Bilinear. Percebe-se que o "pixelamento" diminuiu bastante, contudo o resultado final gerou uma textura mais borrada.

<h3 align = "center">Bilinear</h3>

<br>
<p align = "center">
<img  style = "justify-content: center" src= "prints/akuaku_bilinear.png" alt =   "drawing" width = "306" height = "298">
</p>

<p align = "center">
<b> Figura 2: Aku Aku (Game: Crash Bandicoot) - magFilter: LinearFilter</b><p>
</p>

<h2>Fenômeno de Minificação</h2>


<h3>Filtro de Anisotropia</h3>

Ainda no contexto da minificação, a análise a seguir foi feita levando em consideração os parâmetros padrões de magnificação e minificação do ThreeJs(LinearFilter e LinearMipmapLinearFilter, respectivamente).
Neste âmbito, a metodologia consistiu em  varirar o parâmetro **texture.anisotropy** de modo a atribuí-lo com os valores: 2,4,8 e 16(valores estes citados em sala de aula).  

Em primeiro plano, com a anisotropia igual a 2, pôde-se percerber um borramento na fronteira superior da figura.

<br>
<p align = "center">
<img  style = "justify-content: center" src= "prints/aniso2.png" alt =   "drawing" width = "306" height = "298">
</p>

<p align = "center">
<b> Figura 3: texture.anisotropy: 2</b><p>
</p>


Aumentando a anisotropia para 4 houve um melhoramento da qualidade da imagem, porém ainda com leves borramentos.
<br>
<p align = "center">
<img  style = "justify-content: center" src= "prints/aniso4.png" alt =   "drawing" width = "306" height = "298">
</p>

<p align = "center">
<b> Figura 4: texture.anisotropy: 4</b><p>
</p>

A partir da anisotropia em 8, a qualidade da imagem teve um nítido melhoramento, de modo que não houve muita diferença entre a anisotropia ser 8 ou 16.

<br>
<p align = "center">
<img  style = "justify-content: center" src= "prints/aniso8.png" alt =   "drawing" width = "306" height = "298">
</p>

<p align = "center">
<b> Figura 5: texture.anisotropy: 8</b><p>
</p>

<br>
<p align = "center">
<img  style = "justify-content: center" src= "prints/aniso16.png" alt =   "drawing" width = "306" height = "298">
</p>

<p align = "center">
<b> Figura 6: texture.anisotropy: 16</b><p>
</p>


## Referências

https://sbcode.net/threejs/mipmaps

https://threejsfundamentals.org/threejs/lessons/threejs-textures.html#loading