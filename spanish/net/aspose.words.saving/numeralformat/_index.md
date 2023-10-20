---
title: NumeralFormat Enum
linktitle: NumeralFormat
articleTitle: NumeralFormat
second_title: Aspose.Words para .NET
description: Aspose.Words.Saving.NumeralFormat enumeración. Indica el conjunto de símbolos que se utiliza para representar números mientras se procesa en formatos de página fijos en C#.
type: docs
weight: 5310
url: /es/net/aspose.words.saving/numeralformat/
---
## NumeralFormat enumeration

Indica el conjunto de símbolos que se utiliza para representar números mientras se procesa en formatos de página fijos.

```csharp
public enum NumeralFormat
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| European | `0` | Números europeos: 0123456789. |
| ArabicIndic | `1` | Números utilizados en árabe: ٠١٢٣٤٥٦٧٨٩. Rango Unicode U+0660 - u+0669. |
| EasternArabicIndic | `2` | Números utilizados en persa y urdu: ۰۱۲۳۴۵۶۷۸۹. Rango Unicode U+06F0 - u+06F9. |
| Context | `3` | El conjunto de símbolos se decide a partir del contexto (propiedad regional y RTL). |
| System | `4` | ESTA OPCIÓN NO ES COMPATIBLE. El conjunto de símbolos se decide desde la configuración regional. |

## Ejemplos

Muestra cómo configurar el formato numérico utilizado al guardar en PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.LocaleId = new CultureInfo("ar-AR").LCID;
builder.Writeln("1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Establece la propiedad "NumeralFormat" en "NumeralFormat.ArabicIndic" para
// usa glifos del rango U+0660 a U+0669 como números.
// Establece la propiedad "NumeralFormat" en "NumeralFormat.Context" para
// busca la configuración regional para determinar qué cantidad de glifos usar.
// Establece la propiedad "NumeralFormat" en "NumeralFormat.EasternArabicIndic" para
// usa glifos del rango U+06F0 a U+06F9 como números.
// Establece la propiedad "NumeralFormat" en "NumeralFormat.European" para utilizar números europeos.
// Establezca la propiedad "NumeralFormat" en "NumeralFormat.System" para determinar el conjunto de símbolos a partir de la configuración regional.
options.NumeralFormat = numeralFormat;

doc.Save(ArtifactsDir + "PdfSaveOptions.SetNumeralFormat.pdf", options);
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
