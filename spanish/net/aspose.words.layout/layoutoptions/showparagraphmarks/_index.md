---
title: LayoutOptions.ShowParagraphMarks
linktitle: ShowParagraphMarks
articleTitle: ShowParagraphMarks
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad ShowParagraphMarks de LayoutOptions mejora el formato del texto al activar y desactivar la visibilidad de las marcas de párrafo. ¡Mejore la claridad de sus documentos hoy mismo!
type: docs
weight: 90
url: /es/net/aspose.words.layout/layoutoptions/showparagraphmarks/
---
## LayoutOptions.ShowParagraphMarks property

Obtiene o establece la indicación de si se representan las marcas de párrafo. El valor predeterminado es`FALSO` .

```csharp
public bool ShowParagraphMarks { get; set; }
```

## Ejemplos

Muestra cómo mostrar marcas de párrafo en un documento de salida renderizado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Agregue algunos párrafos y luego habilite las marcas de párrafo para mostrar los finales de los párrafos
// con un símbolo pilcrow (¶) cuando renderizamos el documento.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

### Ver también

* class [LayoutOptions](../)
* espacio de nombres [Aspose.Words.Layout](../../../aspose.words.layout/)
* asamblea [Aspose.Words](../../../)
