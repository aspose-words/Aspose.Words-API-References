---
title: Paragraph.IsEndOfHeaderFooter
linktitle: IsEndOfHeaderFooter
articleTitle: IsEndOfHeaderFooter
second_title: Aspose.Words para .NET
description: Descubra la propiedad IsEndOfHeaderFooter para párrafos. Determine fácilmente si un párrafo es el último de un HeaderFooter, mejorando así la estructura del documento.
type: docs
weight: 70
url: /es/net/aspose.words/paragraph/isendofheaderfooter/
---
## Paragraph.IsEndOfHeaderFooter property

Verdadero si este párrafo es el último párrafo del[`HeaderFooter`](../../headerfooter/) (historia del texto principal) de una[`Section`](../../section/) ; falso en caso contrario.

```csharp
public bool IsEndOfHeaderFooter { get; }
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

* class [Paragraph](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
