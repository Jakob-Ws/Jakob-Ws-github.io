---
title: Die Unendlichkeit der Primzahlen - Der Beweis nach Euclid
layout: post
date: 2024-10-29
author: jakob
permalink: /primzahlen/
---
Es sei angenommen, dass die Menge der Primzahlen \\(\\mathbb{P}\\)
endlich ist. Das bedeutet, dass \\(\\mathbb{P} = \\{p_1, p_2, \\dots,
p_n\\}\\), wobei \\(n \\in \\mathbb{N}\\) und jedes \\(p_i\\) eine
Primzahl ist. Nun wird eine Zahl \\(q\\) konstruiert, indem das Produkt
aller \\(n\\) Primzahlen gebildet und zu diesem Produkt \\(1\\) addiert
wird:

\\\[q = p_1 \\cdot p_2 \\cdot \\dots \\cdot p_n + 1 = \\left(
\\prod\_{i=1}^n p_i \\right) + 1\\\]

Für \\(q\\) ergeben sich zwei mögliche Fälle:

1.  \\(q \\in \\mathbb{P}\\)
2.  \\(q \\notin \\mathbb{P}\\)

Im ersten Fall ergibt sich ein Widerspruch. Da \\(q \\neq p_i\\) für
alle \\(i = 1, \\dots, n\\), existiert eine Primzahl \\(q\\), die nicht
in der ursprünglichen Menge \\(\\mathbb{P}\\) enthalten ist. Dies
widerspricht der Annahme, dass die Menge der Primzahlen endlich ist.

Im zweiten Fall gilt offensichtlich \\(q \\in \\mathbb{N}\\), und nach
dem Fundamentalsatz der Arithmetik hat jede natürliche Zahl größer als 1
mindestens einen Primteiler. Folglich muss auch \\(q\\) einen Primteiler
besitzen.

\\\[\\exists \\: p \\in \\mathbb{P}: \\quad p \\mid q.\\\]

Da \\(p \\in \\mathbb{P}\\) angenommen wird, gilt insbesondere \\(p =
p_i\\) für ein \\(i \\in \\{1, \\dots, n\\}\\). Da \\(p\\) auch das
Produkt \\(p_1 \\cdot p_2 \\cdot \\dots \\cdot p_n\\) teilt, folgt nach
dem Teilbarkeitsgesetz:

\\\[\\begin{align\*} p \\mid q \\quad \\text{und} \\quad p \\mid p_1
\\cdot p_2 \\cdot \\dots \\cdot p_n \\quad &\\Rightarrow \\quad p \\mid
(q - p_1 \\cdot p_2 \\cdot \\dots \\cdot p_n) \\\\ &\\Rightarrow \\quad
p \\mid 1. \\end{align\*}\\\]

Dies stellt einen Widerspruch dar, da keine Primzahl \\(p\\) (mit \\(p
\\neq 1\\)) die Zahl \\(1\\) teilt. Somit ist die Annahme, dass die
Menge der Primzahlen \\(\\mathbb{P}\\) endlich ist, widerlegt. Es folgt,
dass die Menge der Primzahlen unendlich ist.

------------------------------------------------------------------------

Veröffentlicht: 29.Okt.24
