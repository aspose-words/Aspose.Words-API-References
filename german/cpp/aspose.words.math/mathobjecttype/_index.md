---
title: "Aspose::Words::Math::MathObjectType Enum"
linktitle: "MathObjectType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Math::MathObjectType Enum. Gibt den Typ eines Office Math-Objekts in C++ an."
type: docs
weight: 2000
url: /de/cpp/aspose.words.math/mathobjecttype/
---
## MathObjectType enum


Gibt den Typ eines Office [Math](../) Objekts an.

```cpp
enum class MathObjectType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| OMath | 0 | Instanz von mathematischem Text. |
| OMathPara | 1 | [Math](../) Absatz oder Anzeige‑Mathematik‑Zone, die ein oder mehrere [OMath](./) Elemente enthält, die im Anzeigemodus sind. |
| Accent | 2 | Akzentfunktion, bestehend aus einer Basis und einem kombinierenden diakritischen Zeichen. |
| Bar | 3 | Balkenfunktion, bestehend aus einem Basisargument und einem Überstrich oder Unterstrich. |
| BorderBox | 4 | [Border](../../aspose.words/border/) Box-Objekt, bestehend aus einem Rand, der um eine Instanz mathematischen Textes (wie eine Formel oder Gleichung) gezeichnet wird. |
| Box | 5 | Box-Objekt, das verwendet wird, um Komponenten einer Gleichung oder einer anderen Instanz mathematischen Textes zu gruppieren. |
| Delimiter | 6 | Delimiter-Objekt, bestehend aus öffnenden und schließenden Begrenzungszeichen (wie Klammern, geschweiften Klammern, eckigen Klammern und senkrechten Strichen) und einem darin enthaltenen Element. |
| Degree | 7 | Grad im mathematischen Radikal. |
| Argument | 8 | Argument-Objekt. Umschließt Office [Math](../)-Entitäten, wenn sie als Argumente für andere Office [Math](../)-Entitäten verwendet werden. |
| Array | 9 | Array-Objekt, bestehend aus einer oder mehreren Gleichungen, Ausdrücken oder anderen mathematischen Textabschnitten, die vertikal als Einheit im Verhältnis zum umgebenden Text in der Zeile ausgerichtet werden können. |
| Fraction | 10 | Bruch-Objekt, bestehend aus Zähler und Nenner, getrennt durch einen Bruchstrich. |
| Denominator | 11 | Nenner eines Bruch-Objekts. |
| Numerator | 12 | Zähler des Bruch-Objekts. |
| Function | 13 | Function-Apply-Objekt, das aus einem Funktionsnamen und einem darauf angewendeten Argument-Element besteht. |
| FunctionName | 14 | Name der Funktion. Zum Beispiel sind Funktionsnamen sin und cos. |
| GroupCharacter | 15 | Group-Character-Objekt, bestehend aus einem Zeichen, das über oder unter dem Text gezeichnet wird, oft mit dem Zweck, Elemente visuell zu gruppieren. |
| Limit | 16 | Untere Grenze des [LowerLimit](./)-Objekts und die obere Grenze der [UpperLimit](./)-Funktion. |
| LowerLimit | 17 | Lower-Limit-Objekt, bestehend aus Text auf der Grundlinie und verkleinertem Text unmittelbar darunter. |
| UpperLimit | 18 | Upper-Limit-Objekt, bestehend aus Text auf der Grundlinie und verkleinertem Text unmittelbar darüber. |
| Matrix | 19 | Matrix-Objekt, bestehend aus einem oder mehreren Elementen, die in einer oder mehreren Zeilen und einer oder mehreren Spalten angeordnet sind. |
| MatrixRow | 20 | Einzelne Zeile der Matrix. |
| NAry | 21 | N-ary-Objekt, bestehend aus einem n-ary-Objekt, einer Basis (oder Operanden) und optionalen oberen und unteren Grenzen. |
| Phantom | 22 | Phantom-Objekt. |
| Radical | 23 | Radical-Objekt, bestehend aus einem Radikal, einem Basiselement und einem optionalen Grad. |
| SubscriptPart | 24 | Subscript des Objekts, das einen Subscript-Teil haben kann. |
| SuperscriptPart | 25 | Superscript des Superscript-Objekts. |
| PreSubSuperscript | 26 | Pre-Sub-Superscript-Objekt, das aus einem Basiselement sowie einem Subscript und Superscript besteht, die links vom Basiszeichen platziert sind. |
| Subscript | 27 | Tiefgestelltes Objekt, das aus einem Basiselement und einem verkleinerten Skript besteht, das unten und rechts platziert ist. |
| SubSuperskript | 28 | Sub‑Superskript‑Objekt, das aus einem Basiselement, einem verkleinerten Skript unten und rechts sowie einem verkleinerten Skript oben und rechts besteht. |
| Superskript | 29 | Superskript‑Objekt, das aus einem Basiselement und einem verkleinerten Skript besteht, das oben und rechts platziert ist. |
| Keine | 30 | Der Objekttyp ist nicht angegeben. |

## Siehe auch

* Namespace [Aspose::Words::Math](../)
* Library [Aspose.Words for C++](../../)
