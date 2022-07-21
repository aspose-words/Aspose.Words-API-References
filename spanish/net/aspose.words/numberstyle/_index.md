---
title: NumberStyle
second_title: Referencia de API de Aspose.Words para .NET
description: Especifica el estilo de número para una lista notas al pie y notas al final números de página.
type: docs
weight: 4070
url: /es/net/aspose.words/numberstyle/
---
## NumberStyle enumeration

Especifica el estilo de número para una lista, notas al pie y notas al final, números de página.

```csharp
public enum NumberStyle
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Arabic | `0` | Numeración arábiga (1, 2, 3, ...) |
| UppercaseRoman | `1` | Mayúsculas romanas (I, II, III, ...) |
| LowercaseRoman | `2` | Romano en minúsculas (i, ii, iii, ...) |
| UppercaseLetter | `3` | Letra mayúscula (A, B, C, ...) |
| LowercaseLetter | `4` | Letra minúscula (a, b, c, ...) |
| Ordinal | `5` | Ordinal (1º, 2º, 3º, ...) |
| Number | `6` | Numerado (Uno, Dos, Tres, ...) |
| OrdinalText | `7` | Ordinal (texto) (Primero, Segundo, Tercero, ...) |
| Hex | `8` | Hexadecimal: 8, 9, A, B, C, D, E, F, 10, 11, 12 |
| ChicagoManual | `9` | Manual de estilo de Chicago: *, †, † |
| Kanji | `10` | Ideograph-digital |
| KanjiDigit | `11` | conteo japonés |
| AiueoHalfWidth | `12` | Aiueo |
| IrohaHalfWidth | `13` | Iroha |
| ArabicFullWidth | `14` | Árabe de ancho completo: 1, 2, 3, 4 |
| ArabicHalfWidth | `15` | Árabe de ancho medio: 1, 2, 3, 4 |
| KanjiTraditional | `16` | Japonés legal |
| KanjiTraditional2 | `17` | Diez mil digitales japoneses |
| NumberInCircle | `18` | Círculos cerrados |
| DecimalFullWidth | `19` | Ancho total decimal: 1, 2, 3, 4 |
| Aiueo | `20` | Aiueo ancho completo |
| Iroha | `21` | Iroha ancho completo |
| LeadingZero | `22` | Cero inicial (01, 02,..., 09, 10, 11,..., 99, 100, 101,...) |
| Bullet | `23` | Viñeta (compruebe el código de carácter en el texto) |
| Ganada | `24` | Coreano Ganada |
| Chosung | `25` | Corea Chosung |
| GB1 | `26` | Punto cerrado completo |
| GB2 | `27` | Paréntesis adjunto |
| GB3 | `28` | Círculo cerrado Chino |
| GB4 | `29` | Círculo cerrado de ideograma |
| Zodiac1 | `30` | Ideograma tradicional |
| Zodiac2 | `31` | Ideograma Zodíaco |
| Zodiac3 | `32` | Ideograma Zodíaco tradicional |
| TradChinNum1 | `33` | conteo taiwanés |
| TradChinNum2 | `34` | Ideografía legal tradicional |
| TradChinNum3 | `35` | Taiwaneses contando mil |
| TradChinNum4 | `36` | digital taiwanés |
| SimpChinNum1 | `37` | conteo chino |
| SimpChinNum2 | `38` | Chino legal simplificado |
| SimpChinNum3 | `39` | chino contando mil |
| SimpChinNum4 | `40` | Chino (no implementado) |
| HanjaRead | `41` | digital coreano |
| HanjaReadDigit | `42` | conteo coreano |
| Hangul | `43` | Corea legal |
| Hanja | `44` | Corea digital2 |
| Hebrew1 | `45` | Hebreo-1 |
| Arabic1 | `46` | árabe alfa |
| Hebrew2 | `47` | Hebreo-2 |
| Arabic2 | `48` | Árabe abjad |
| HindiLetter1 | `49` | Vocales hindi |
| HindiLetter2 | `50` | consonantes hindi |
| HindiArabic | `51` | Números en hindi |
| HindiCardinalText | `52` | Hindi descriptivo (cardinales) |
| ThaiLetter | `53` | letras tailandesas |
| ThaiArabic | `54` | números tailandeses |
| ThaiCardinalText | `55` | Descriptivo tailandés (cardinales) |
| VietCardinalText | `56` | Descriptivo vietnamita (cardinales) |
| NumberInDash | `57` | Formato de número de página: - 1 -, - 2 -, - 3 -, - 4 - |
| LowercaseRussian | `58` | Alfabeto ruso en minúsculas |
| UppercaseRussian | `59` | Alfabeto ruso en mayúsculas |
| None | `255` | Sin viñeta ni número. |
| Custom | `65280` | Formato de número personalizado. Solo es compatible con el formato DOCX. |

### Ejemplos

Muestra cómo aplicar un formato de lista personalizado a los párrafos cuando se usa DocumentBuilder.

```csharp
Document doc = new Document();

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
// Podemos crear listas anidadas aumentando el nivel de sangría. 
// Podemos comenzar y finalizar una lista usando la propiedad "ListFormat" del generador de documentos. 
// Cada párrafo que agreguemos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
// Cree una lista a partir de una plantilla de Microsoft Word y personalice los dos primeros niveles de la lista.
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

// Este valor de NumberFormat creará símbolos de lista de viñetas en forma de estrella.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// Crear párrafos y aplicarles ambos niveles de lista de nuestro formato de lista personalizado.
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

* espacio de nombres [Aspose.Words](../../aspose.words)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
