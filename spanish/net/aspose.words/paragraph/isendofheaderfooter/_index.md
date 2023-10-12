---
title: Paragraph.IsEndOfHeaderFooter
second_title: Referencia de API de Aspose.Words para .NET
description: Paragraph propiedad. Verdadero si este párrafo es el último párrafo delHeaderFooter historia del texto principal de unSection  falso en caso contrario.
type: docs
weight: 70
url: /es/net/aspose.words/paragraph/isendofheaderfooter/
---
## Paragraph.IsEndOfHeaderFooter property

Verdadero si este párrafo es el último párrafo del[`HeaderFooter`](../../headerfooter/) (historia del texto principal) de un[`Section`](../../section/) ; falso en caso contrario.

```csharp
public bool IsEndOfHeaderFooter { get; }
```

### Ejemplos

Muestra cómo crear un encabezado y un pie de página.

```csharp
Document doc = new Document();

// Crea un encabezado y añádele un párrafo. El texto de ese párrafo
// aparecerá en la parte superior de cada página de esta sección, encima del texto del cuerpo principal.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Crea un pie de página y añádele un párrafo. El texto de ese párrafo
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
* espacio de nombres [Aspose.Words](../../paragraph/)
* asamblea [Aspose.Words](../../../)


