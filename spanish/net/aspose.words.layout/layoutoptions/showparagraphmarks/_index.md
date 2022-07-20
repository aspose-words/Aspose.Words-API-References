---
title: ShowParagraphMarks
second_title: Referencia de API de Aspose.Words para .NET
description: Obtiene o establece la indicación de si se representan las marcas de párrafo. El valor predeterminado es Falso.
type: docs
weight: 80
url: /es/net/aspose.words.layout/layoutoptions/showparagraphmarks/
---
## LayoutOptions.ShowParagraphMarks property

Obtiene o establece la indicación de si se representan las marcas de párrafo. El valor predeterminado es Falso.

```csharp
public bool ShowParagraphMarks { get; set; }
```

### Ejemplos

Muestra cómo mostrar marcas de párrafo en un documento de salida renderizado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Agregue algunos párrafos, luego habilite las marcas de párrafo para mostrar los extremos de los párrafos
// con un símbolo de almohada (¶) cuando renderizamos el documento.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

### Ver también

* class [LayoutOptions](../../layoutoptions)
* espacio de nombres [Aspose.Words.Layout](../../layoutoptions)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->