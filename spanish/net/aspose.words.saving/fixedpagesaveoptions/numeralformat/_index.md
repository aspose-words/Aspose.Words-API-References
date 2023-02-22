---
title: FixedPageSaveOptions.NumeralFormat
second_title: Referencia de API de Aspose.Words para .NET
description: FixedPageSaveOptions propiedad. Obtiene o estableceNumeralFormat se utiliza para representar números. Los números europeos se utilizan de forma predeterminada.
type: docs
weight: 40
url: /es/net/aspose.words.saving/fixedpagesaveoptions/numeralformat/
---
## FixedPageSaveOptions.NumeralFormat property

Obtiene o establece[`NumeralFormat`](../../numeralformat/) se utiliza para representar números. Los números europeos se utilizan de forma predeterminada.

```csharp
public NumeralFormat NumeralFormat { get; set; }
```

### Observaciones

Si se cambia el valor de esta propiedad y el diseño de la página ya está construido entonces [`UpdatePageLayout`](../../../aspose.words/document/updatepagelayout/) se invoca automáticamente para actualizar cualquier cambio.

### Ejemplos

Muestra cómo configurar el formato numérico utilizado al guardar en PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.LocaleId = new CultureInfo("ar-AR").LCID;
builder.Writeln("1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Establecer la propiedad "NumeralFormat" en "NumeralFormat.ArabicIndic" para
// usa glifos del rango U+0660 a U+0669 como números.
// Establecer la propiedad "NumeralFormat" en "NumeralFormat.Context" para
// busque la configuración regional para determinar qué número de glifos usar.
// Establecer la propiedad "NumeralFormat" en "NumeralFormat.EasternArabicIndic" para
// usa glifos del rango U+06F0 a U+06F9 como números.
// Establezca la propiedad "NumeralFormat" en "NumeralFormat.European" para usar números europeos.
// Establezca la propiedad "NumeralFormat" en "NumeralFormat.System" para determinar el conjunto de símbolos de la configuración regional.
options.NumeralFormat = numeralFormat;

doc.Save(ArtifactsDir + "PdfSaveOptions.SetNumeralFormat.pdf", options);
```

### Ver también

* enum [NumeralFormat](../../numeralformat/)
* class [FixedPageSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../fixedpagesaveoptions/)
* asamblea [Aspose.Words](../../../)


