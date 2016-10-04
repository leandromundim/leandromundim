---
layout: post
title: "Como calcular área de um polígono"
date: 2016-09-23 00:00:00
description: 'Calculando área de polígonos convexos e não convexos em C.'
main-class: 'lrm'
color: '#AA7F39'
tags:
- C
- area
- polígono
image: "/assets/img/digital-nomad.jpg"
categories:
twitter_text: 'Formula fechada para calcular área de polígonos convexos e não convexos. '
introduction: "Código em C, muito simples, para o cálculo de áreas de polígonos."
---

Considere um polígono simples, sem auto interseção. 

Entrada:
<b>X, Y</b> são vetores, de tamanho <b>n</b>, com as coordenadas cartesianas do polígono.

Saída:
A área do polígono.

{% highlight c %}
function area(X, Y, n){
  area = 0;        
  j = n-1;  
  for (i=0; i<n; i++){ 
    area = area +  (X[j]+X[i]) * (Y[j]-Y[i]);
    j = i;  
  }
  return abs(area/2);
}
{% endhighlight %}
