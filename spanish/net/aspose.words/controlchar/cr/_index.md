---
title: Cr
second_title: Referencia de API de Aspose.Words para .NET
description: Carácter de retorno de carro x000d o r. Igual queParagraphBreakaspose.words/controlchar/paragraphbreak .
type: docs
weight: 50
url: /es/net/aspose.words/controlchar/cr/
---
## ControlChar.Cr field

Carácter de retorno de carro: "\x000d" o "\r". Igual que[`ParagraphBreak`](../paragraphbreak) .

```csharp
public static readonly string Cr;
```

### Ejemplos

Muestra cómo usar los caracteres de control.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar párrafos con texto con DocumentBuilder.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Convertir el documento a formato de texto revela que los caracteres de control
// representar algunos de los elementos estructurales del documento, como los saltos de página.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// Al convertir un documento a formato de cadena,
// podemos omitir algunos de los caracteres de control con el método Trim.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### Ver también

* class [ControlChar](../../controlchar)
* espacio de nombres [Aspose.Words](../../controlchar)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
