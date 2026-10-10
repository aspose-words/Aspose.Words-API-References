---
title: "Aspose::Words::Math::MathObjectType enum"
linktitle: "MathObjectType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Math::MathObjectType enum. Anger typen av ett Office Math-objekt i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.math/mathobjecttype/
---
## MathObjectType enum


Anger typen av ett Office [Math](../) objekt.

```cpp
enum class MathObjectType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| OMath | 0 | Instans av matematisk text. |
| OMathPara | 1 | [Math](../) stycke, eller display-matematikzon, som innehåller ett eller flera [OMath](./) element som är i displayläge. |
| Accent | 2 | Accentfunktion, bestående av en bas och ett kombinerande diakritiskt tecken. |
| Bar | 3 | Bar-funktion, bestående av ett basargument och en överstreck eller understreck. |
| BorderBox | 4 | [Border](../../aspose.words/border/) Box-objekt, bestående av en ram som ritas runt en instans av matematisk text (såsom en formel eller ekvation) |
| Box | 5 | Box-objekt, som används för att gruppera komponenter i en ekvation eller annan instans av matematisk text. |
| Avgränsare | 6 | Avgränsare-objekt, bestående av öppnings- och stängningsavgränsare (såsom parenteser, klammerparenteser, hakparenteser och vertikala streck), samt ett element som finns inuti. |
| Grad | 7 | Grad i den matematiska roten. |
| Argument | 8 | Argument-objekt. Omsluter Office [Math](../)-entiteter när de används som argument till andra Office [Math](../)-entiteter. |
| Array | 9 | Array-objekt, bestående av en eller flera ekvationer, uttryck eller annan matematisk text som kan vertikalt justeras som en enhet i förhållande till omgivande text på raden. |
| Bråk | 10 | Bråk-objekt, bestående av en täljare och en nämnare separerade av ett bråkstreck. |
| Nämnare | 11 | Nämnare för ett bråk-objekt. |
| Täljare | 12 | Täljare för Bråk-objektet. |
| Funktion | 13 | Function-Apply-objekt, som består av ett funktionsnamn och ett argumentelement som påverkas. |
| FunctionName | 14 | Namn på funktionen. Till exempel är funktionsnamn sin och cos. |
| GroupCharacter | 15 | Group-Character-objekt, bestående av ett tecken som ritas ovanför eller under text, ofta med syftet att visuellt gruppera objekt. |
| Limit | 16 | Nedre gräns för [LowerLimit](./)-objektet och övre gränsen för [UpperLimit](./)-funktionen. |
| LowerLimit | 17 | Lower-Limit-objekt, bestående av text på baslinjen och förminskad text omedelbart under den. |
| UpperLimit | 18 | Upper-Limit-objekt, bestående av text på baslinjen och förminskad text omedelbart ovanför den. |
| Matrix | 19 | Matrix-objekt, bestående av ett eller flera element placerade i en eller flera rader och en eller flera kolumner. |
| MatrixRow | 20 | En enda rad i matrisen. |
| NAry | 21 | N-ary-objekt, bestående av ett n-ary-objekt, en bas (eller operand) och valfria övre och nedre gränser. |
| Phantom | 22 | Phantom-objekt. |
| Radical | 23 | Radical-objekt, bestående av en radikal, ett baselement och en valfri grad. |
| SubscriptPart | 24 | Nedsänkt av objektet som kan ha en nedsänkt del. |
| SuperscriptPart | 25 | Upphöjd av superscript-objektet. |
| PreSubSuperscript | 26 | Pre-Sub-Superscript-objekt, bestående av ett baselement samt en nedsänkt och en upphöjd placeras till vänster om basen. |
| Subscript | 27 | Subscript-objekt, bestående av ett baselement och ett förminskat skript placerat nedanför och till höger. |
| SubSuperscript | 28 | Sub-superscript-objekt, bestående av ett baselement, ett förminskat skript placerat nedanför och till höger samt ett förminskat skript placerat ovanför och till höger. |
| Superscript | 29 | Superscript-objekt, bestående av ett baselement och ett förminskat skript placerat ovanför och till höger. |
| None | 30 | Typ av objekt är inte specificerad. |

## Se även

* Namespace [Aspose::Words::Math](../)
* Library [Aspose.Words for C++](../../)
