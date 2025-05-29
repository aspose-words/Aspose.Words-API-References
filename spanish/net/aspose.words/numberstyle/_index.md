---
title: NumberStyle Enum
linktitle: NumberStyle
articleTitle: NumberStyle
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.NumberStyle para personalizar los números de página de notas al pie y notas finales, mejorando el formato de su documento sin esfuerzo.
type: docs
weight: 5040
url: /es/net/aspose.words/numberstyle/
---
## NumberStyle enumeration

Especifica el estilo de número para una lista, notas al pie y notas finales, números de página.

```csharp
public enum NumberStyle
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Arabic | `0` | Numeración árabe (1, 2, 3, ...) |
| UppercaseRoman | `1` | Mayúsculas romanas (I, II, III, ...) |
| LowercaseRoman | `2` | Letras romanas minúsculas (i, ii, iii, ...) |
| UppercaseLetter | `3` | Letra mayúscula (A, B, C, ...) |
| LowercaseLetter | `4` | Letra minúscula (a, b, c, ...) |
| Ordinal | `5` | Ordinal (1º, 2º, 3º, ...) |
| Number | `6` | Numerados (Uno, Dos, Tres, ...) |
| OrdinalText | `7` | Ordinal (texto) (Primero, Segundo, Tercero, ...) |
| Hex | `8` | Hexadecimal: 8, 9, A, B, C, D, E, F, 10, 11, 12 |
| ChicagoManual | `9` | Manual de estilo de Chicago: *, †, † |
| Kanji | `10` | Ideograma-digital |
| KanjiDigit | `11` | Conteo japonés |
| AiueoHalfWidth | `12` | Aiueo |
| IrohaHalfWidth | `13` | Iroha |
| ArabicFullWidth | `14` | Árabe de ancho completo: 1, 2, 3, 4 |
| ArabicHalfWidth | `15` | Árabe de ancho medio: 1, 2, 3, 4 |
| KanjiTraditional | `16` | Legal japonés |
| KanjiTraditional2 | `17` | Diez mil digitales japoneses |
| NumberInCircle | `18` | Círculos cerrados |
| DecimalFullWidth | `19` | Ancho completo decimal: 1, 2, 3, 4 |
| Aiueo | `20` | Aiueo ancho completo |
| Iroha | `21` | Iroha ancho completo |
| LeadingZero | `22` | Cero inicial (01, 02,..., 09, 10, 11,..., 99, 100, 101,...) |
| Bullet | `23` | Bala (verifique el código de carácter en el texto) |
| Ganada | `24` | Coreana Ganada |
| Chosung | `25` | Corea Chosung |
| GB1 | `26` | Punto final adjunto |
| GB2 | `27` | Paréntesis cerrado |
| GB3 | `28` | Círculo cerrado Chino |
| GB4 | `29` | Ideógrafo círculo cerrado |
| Zodiac1 | `30` | Ideógrafo tradicional |
| Zodiac2 | `31` | Ideógrafo del Zodíaco |
| Zodiac3 | `32` | Ideógrafo del zodíaco tradicional |
| TradChinNum1 | `33` | Conteo taiwanés |
| TradChinNum2 | `34` | Ideógrafo legal tradicional |
| TradChinNum3 | `35` | Taiwanés contando mil |
| TradChinNum4 | `36` | Digital taiwanés |
| SimpChinNum1 | `37` | Conteo chino |
| SimpChinNum2 | `38` | Legal chino simplificado |
| SimpChinNum3 | `39` | Conteo chino de mil |
| SimpChinNum4 | `40` | Chino (no implementado) |
| HanjaRead | `41` | Digital coreano |
| HanjaReadDigit | `42` | Conteo coreano |
| Hangul | `43` | Corea legal |
| Hanja | `44` | Corea digital2 |
| Hebrew1 | `45` | Hebreo-1 |
| Arabic1 | `46` | Alfa árabe |
| Hebrew2 | `47` | Hebreo-2 |
| Arabic2 | `48` | Árabe abjad |
| HindiLetter1 | `49` | Vocales del hindi |
| HindiLetter2 | `50` | Consonantes hindi |
| HindiArabic | `51` | Números en hindi |
| HindiCardinalText | `52` | Hindi descriptivo (cardinales) |
| ThaiLetter | `53` | Letras tailandesas |
| ThaiArabic | `54` | Números tailandeses |
| ThaiCardinalText | `55` | Descriptivo tailandés (cardinales) |
| VietCardinalText | `56` | Descriptivo vietnamita (cardinales) |
| NumberInDash | `57` | Formato de número de página: - 1 -, - 2 -, - 3 -, - 4 - |
| LowercaseRussian | `58` | Alfabeto ruso en minúsculas |
| UppercaseRussian | `59` | Alfabeto ruso en mayúsculas |
| None | `255` | Sin viñeta ni número. |
| Custom | `65280` | Formato de número personalizado. Solo compatible con el formato DOCX. |

## Ejemplos

Muestra cómo aplicar formato de lista personalizado a los párrafos cuando se utiliza DocumentBuilder.

```csharp
Document doc = new Document();

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
 //Podemos crear listas anidadas aumentando el nivel de sangría.
 // Podemos comenzar y finalizar una lista utilizando la propiedad "ListFormat" de un generador de documentos.
//Cada párrafo que agreguemos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
// Cree una lista a partir de una plantilla de Microsoft Word y personalice los dos primeros niveles de lista.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

ListLevel listLevel = list.ListLevels[0];
listLevel.Font.Color = Color.Red;
listLevel.Font.Size = 24;
listLevel.NumberStyle = NumberStyle.OrdinalText;
listLevel.StartAt = 21;
listLevel.NumberFormat = "\x0000";

listLevel.NumberPosition = -36;
listLevel.TextPosition = 144;
listLevel.TabPosition = 144;

listLevel = list.ListLevels[1];
listLevel.Alignment = ListLevelAlignment.Right;
listLevel.NumberStyle = NumberStyle.Bullet;
listLevel.Font.Name = "Wingdings";
listLevel.Font.Color = Color.Blue;
listLevel.Font.Size = 24;

// Este valor de NumberFormat creará símbolos de lista con viñetas en forma de estrella.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// Cree párrafos y aplíqueles ambos niveles de lista de nuestro formato de lista personalizado.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("The quick brown fox...");
builder.Writeln("The quick brown fox...");

builder.ListFormat.ListIndent();
builder.Writeln("jumped over the lazy dog.");
builder.Writeln("jumped over the lazy dog.");

builder.ListFormat.ListOutdent();
builder.Writeln("The quick brown fox...");

builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateCustomList.docx");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
