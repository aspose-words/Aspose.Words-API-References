---
title: GeneralFormat
second_title: Referencia de API de Aspose.Words para .NET
description: Especifica un formato general que se aplica a un resultado numérico de texto o de cualquier campo. Un campo puede tener una combinación de formatos generales.
type: docs
weight: 2480
url: /es/net/aspose.words.fields/generalformat/
---
## GeneralFormat enumeration

Especifica un formato general que se aplica a un resultado numérico, de texto o de cualquier campo. Un campo puede tener una combinación de formatos generales.

```csharp
public enum GeneralFormat
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | Se usa para especificar un formato general faltante. |
| Aiueo | `1` | Formato numérico. Da formato a un resultado numérico usando caracteres hiragana en el orden tradicional de aiueo. |
| UppercaseAlphabetic | `2` | Formato numérico. Da formato a un resultado numérico como una o más apariciones de un carácter latino alfabético en mayúsculas. |
| LowercaseAlphabetic | `3` | Formato numérico. Da formato a un resultado numérico como una o más apariciones de un carácter latino alfabético en minúsculas. |
| Arabic | `4` | Formato numérico. Da formato a un resultado numérico usando números cardinales arábigos. |
| ArabicAbjad | `5` | Formato numérico. Da formato a un resultado numérico utilizando números Abjad ascendentes. |
| ArabicAlpha | `6` | Formato numérico. Da formato a un resultado numérico utilizando caracteres del alfabeto árabe. |
| ArabicDash | `7` | Formato numérico. Da formato a un resultado numérico usando números cardinales arábigos, con un prefijo "-" y un sufijo "-". |
| BahtText | `8` | Formato numérico. Da formato a un resultado numérico en el sistema de conteo tailandés. |
| CardText | `9` | Formato numérico. Texto cardinal (Uno, Dos, Tres, ...). |
| ChineseNum1 | `10` | Formato numérico. Da formato a un resultado numérico usando números ascendentes del sistema de conteo apropiado. |
| ChineseNum2 | `11` | Formato numérico. Da formato a un resultado numérico usando números secuenciales del formato legal apropiado. |
| ChineseNum3 | `12` | Formato numérico. Da formato a un resultado numérico usando números secuenciales del sistema de conteo de miles apropiado. |
| Chosung | `13` | Formato numérico. Da formato a un resultado numérico utilizando números secuenciales del formato coreano Chosung. |
| CircleNum | `14` | Formato numérico. Da formato a un resultado numérico usando numeración decimal dentro de un círculo, usando el carácter de glifo alfanumérico encerrado para números en el rango 1–20. |
| DBChar | `15` | Formato numérico. Da formato a un resultado numérico usando numeración arábiga de doble byte. |
| DBNum1 | `16` | Formato numérico. Da formato a un resultado numérico usando ideogramas digitales secuenciales, usando el carácter apropiado. |
| DBNum2 | `17` | Formato numérico. Da formato a un resultado numérico usando números secuenciales del sistema de conteo apropiado. |
| DBNum3 | `18` | Formato numérico. Da formato a un resultado numérico usando números secuenciales del sistema de conteo legal apropiado. |
| DBNum4 | `19` | Formato numérico. Da formato a un resultado numérico usando números secuenciales del sistema de conteo digital apropiado. |
| DollarText | `20` | Formato numérico. Texto en dólares (Uno, Dos, Tres, ... + Y 55/100). |
| Ganada | `21` | Formato numérico. Da formato a un resultado numérico utilizando números secuenciales del formato coreano de Ganada. |
| GB1 | `22` | Formato numérico. Da formato a un resultado numérico usando numeración decimal seguida de un punto, usando el carácter de glifo alfanumérico adjunto. |
| GB2 | `23` | Formato numérico. Da formato a un resultado numérico usando la numeración decimal encerrada entre paréntesis, usando el carácter de glifo alfanumérico adjunto. |
| GB3 | `24` | Formato numérico. Da formato a un resultado numérico usando numeración decimal encerrada en un círculo, usando el carácter de glifo alfanumérico encerrado . |
| GB4 | `25` | Formato numérico. Da formato a un resultado numérico usando numeración decimal encerrada en un círculo, usando el carácter de glifo alfanumérico encerrado . |
| Hebrew1 | `26` | Formato numérico. Da formato a un resultado numérico usando números hebreos. |
| Hebrew2 | `27` | Formato numérico. Da formato a un resultado numérico utilizando el alfabeto hebreo. |
| Hex | `28` | Formato numérico. Da formato al resultado numérico utilizando dígitos hexadecimales en mayúsculas. |
| HindiArabic | `29` | Formato numérico. Da formato a un resultado numérico utilizando números en hindi. |
| HindiCardText | `30` | Formato numérico. Da formato a un resultado numérico usando números secuenciales del sistema de conteo hindi. |
| HindiLetter1 | `31` | Formato numérico. Da formato a un resultado numérico utilizando vocales hindi. |
| HindiLetter2 | `32` | Formato numérico. Da formato a un resultado numérico utilizando consonantes hindi. |
| Iroha | `33` | Formato numérico. Da formato a un resultado numérico usando el japonés iroha. |
| KanjiNum1 | `34` | Formato numérico. Da formato a un resultado numérico usando un estilo japonés usando el sistema de conteo apropiado. |
| KanjiNum2 | `35` | Formato numérico. Da formato a un resultado numérico usando el sistema de conteo apropiado. |
| KanjiNum3 | `36` | Formato numérico. Da formato a un resultado numérico usando el sistema de conteo apropiado. |
| Ordinal | `37` | Formato numérico. Ordinales (1º, 2º, 3º, ...). |
| OrdText | `38` | Formato numérico. Texto ordinal (Primero, Segundo, Tercero, ...). |
| UppercaseRoman | `39` | Formato numérico. Mayúsculas romanas (I, II, III, ...). |
| LowercaseRoman | `40` | Formato numérico. Romano en minúsculas (i, ii, iii, ...). |
| SBChar | `41` | Formato numérico. Da formato a un resultado numérico usando numeración arábiga de un solo byte. |
| ThaiArabic | `42` | Formato numérico. Da formato a un resultado numérico usando números tailandeses. |
| ThaiCardText | `43` | Formato numérico. Da formato a un resultado numérico usando números secuenciales del sistema de conteo tailandés. |
| ThaiLetter | `44` | Formato numérico. Da formato a un resultado numérico utilizando letras tailandesas. |
| VietCardText | `45` | Formato numérico. Da formato a un resultado numérico utilizando números vietnamitas. |
| Zodiac1 | `46` | Formato numérico. Da formato a un resultado numérico utilizando ideogramas tradicionales numéricos secuenciales. |
| Zodiac2 | `47` | Formato numérico. Da formato a un resultado numérico utilizando ideogramas zodiacales secuenciales. |
| Zodiac3 | `48` | Formato numérico. Da formato a un resultado numérico utilizando ideogramas secuenciales tradicionales del zodíaco. |
| Caps | `49` | Formato de texto. Pone en mayúscula la primera letra de cada palabra. |
| FirstCap | `50` | Formato de texto. Pone en mayúscula la primera letra de la primera palabra. |
| Lower | `51` | Formato de texto. Todas las letras son minúsculas. |
| Upper | `52` | Formato de texto. Todas las letras están en mayúsculas. |
| CharFormat | `53` | Formato de resultado de campo. La instrucción CHARFORMAT. |
| MergeFormat | `54` | Formato de resultado de campo. La instrucción MERGEFORMAT. |
| MergeFormatInet | `55` | Formato de resultado de campo. La instrucción MERGEFORMATINET. |

### Ejemplos

Muestra cómo dar formato a los resultados de los campos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Use un generador de documentos para insertar un campo que muestre un resultado sin formato aplicado.
Field field = builder.InsertField("= 2 + 3");

Assert.AreEqual("= 2 + 3", field.GetFieldCode());
Assert.AreEqual("5", field.Result);

// Podemos aplicar un formato al resultado de un campo usando las propiedades del campo.
// A continuación se muestran tres tipos de formatos que podemos aplicar al resultado de un campo.
// 1 - Formato numérico:
FieldFormat format = field.Format;
format.NumericFormat = "$###.00";
field.Update();

Assert.AreEqual("= 2 + 3 \\# $###.00", field.GetFieldCode());
Assert.AreEqual("$  5.00", field.Result);

// 2 - Formato de fecha/hora:
field = builder.InsertField("DATE");
format = field.Format;
format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());
Console.WriteLine($"Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

// 3 - Formato general:
field = builder.InsertField("= 25 + 33");
format = field.Format;
format.GeneralFormats.Add(GeneralFormat.LowercaseRoman);
format.GeneralFormats.Add(GeneralFormat.Upper);
field.Update();

int index = 0;
using (IEnumerator<GeneralFormat> generalFormatEnumerator = format.GeneralFormats.GetEnumerator())
    while (generalFormatEnumerator.MoveNext())
        Console.WriteLine($"General format index {index++}: {generalFormatEnumerator.Current}");

Assert.AreEqual("= 25 + 33 \\* roman \\* Upper", field.GetFieldCode());
Assert.AreEqual("LVIII", field.Result);
Assert.AreEqual(2, format.GeneralFormats.Count);
Assert.AreEqual(GeneralFormat.LowercaseRoman, format.GeneralFormats[0]);

// Podemos eliminar nuestros formatos para revertir el resultado del campo a su forma original.
format.GeneralFormats.Remove(GeneralFormat.LowercaseRoman);
format.GeneralFormats.RemoveAt(0);
Assert.AreEqual(0, format.GeneralFormats.Count);
field.Update();

Assert.AreEqual("= 25 + 33  ", field.GetFieldCode());
Assert.AreEqual("58", field.Result);
Assert.AreEqual(0, format.GeneralFormats.Count);
```

### Ver también

* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
