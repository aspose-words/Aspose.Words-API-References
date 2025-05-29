---
title: Paragraph.ParentStory
linktitle: ParentStory
articleTitle: ParentStory
second_title: Aspose.Words para .NET
description: Descubra la propiedad Párrafo ParentStory para acceder fácilmente a las historias de nivel de sección principal y mejorar la estructura de su documento con las opciones Cuerpo o Encabezado y Pie de página.
type: docs
weight: 210
url: /es/net/aspose.words/paragraph/parentstory/
---
## Paragraph.ParentStory property

Recupera la historia a nivel de sección principal que se puede[`Body`](../../body/) o[`HeaderFooter`](../../headerfooter/) .

```csharp
public Story ParentStory { get; }
```

## Ejemplos

Muestra cómo crear un encabezado y un pie de página.

```csharp
Document doc = new Document();

// Crea un encabezado y añade un párrafo. El texto de ese párrafo
// aparecerá en la parte superior de cada página de esta sección, encima del texto del cuerpo principal.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Crea un pie de página y añade un párrafo. El texto de ese párrafo
// aparecerá en la parte inferior de cada página de esta sección, debajo del texto del cuerpo principal.
HeaderFooter footer = new HeaderFooter(doc, HeaderFooterType.FooterPrimary);
doc.FirstSection.HeadersFooters.Add(footer);

para = footer.AppendParagraph("My footer.");

Assert.False(footer.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

Assert.AreEqual(footer, para.ParentStory);
Assert.AreEqual(footer.ParentSection, para.ParentSection);
Assert.AreEqual(footer.ParentSection, header.ParentSection);

doc.Save(ArtifactsDir + "HeaderFooter.Create.docx");
```

### Ver también

* class [Story](../../story/)
* class [Paragraph](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
