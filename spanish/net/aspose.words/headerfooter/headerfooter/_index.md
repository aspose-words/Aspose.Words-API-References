---
title: HeaderFooter.HeaderFooter
second_title: Referencia de API de Aspose.Words para .NET
description: HeaderFooter constructor. Crea un nuevo encabezado o pie de página del tipo especificado.
type: docs
weight: 10
url: /es/net/aspose.words/headerfooter/headerfooter/
---
## HeaderFooter constructor

Crea un nuevo encabezado o pie de página del tipo especificado.

```csharp
public HeaderFooter(DocumentBase doc, HeaderFooterType headerFooterType)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| doc | DocumentBase | El documento del propietario. |
| headerFooterType | HeaderFooterType | A[`HeaderFooterType`](../headerfootertype/) value que especifica el tipo de encabezado o pie de página. |

### Observaciones

Cuando[`HeaderFooter`](../) se crea, pertenece al documento especificado, pero aún no es parte del documento y[`ParentNode`](../../node/parentnode/) es`nulo`.

Para anexar[`HeaderFooter`](../) un[`Section`](../../section/) usarNode) ,Node) , o[`HeadersFooters`](../../section/headersfooters/) propiedades y métodos[`Add`](../../nodecollection/add/) ,[`Insert`](../../nodecollection/insert/).

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

* class [DocumentBase](../../documentbase/)
* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooter](../)
* espacio de nombres [Aspose.Words](../../headerfooter/)
* asamblea [Aspose.Words](../../../)


