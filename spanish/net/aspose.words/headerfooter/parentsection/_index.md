---
title: HeaderFooter.ParentSection
second_title: Referencia de API de Aspose.Words para .NET
description: HeaderFooter propiedad. Obtiene la sección principal de esta historia.
type: docs
weight: 60
url: /es/net/aspose.words/headerfooter/parentsection/
---
## HeaderFooter.ParentSection property

Obtiene la sección principal de esta historia.

```csharp
public Section ParentSection { get; }
```

### Observaciones

`ParentSection` es equivalente a[`ParentNode`](../../node/parentnode/) lanzado a[`Section`](../../section/).

### Ejemplos

Muestra cómo vincular encabezados y pies de página entre secciones.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 3");

// Pasa a la primera sección y crea un encabezado y un pie de página. Por defecto,
// el encabezado y el pie de página solo aparecerán en las páginas de la sección que los contiene.
builder.MoveToSection(0);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header, which will be displayed in sections 1 and 2.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// Podemos vincular los encabezados/pies de página de una sección a los encabezados/pies de página de la sección anterior
// para permitir que la sección de enlace muestre los encabezados/pies de página de la sección enlazada.
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

// Cada sección seguirá teniendo sus propios objetos de encabezado/pie de página. Cuando vinculamos secciones,
// la sección de enlace mostrará el encabezado/pie de página de la sección enlazada manteniendo los suyos propios.
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// Vincula los encabezados/pies de página de la tercera sección a los encabezados/pies de página de la segunda sección.
// La segunda sección ya enlaza con el encabezado/pie de página de la primera sección,
// por lo que vincular a la segunda sección creará una cadena de vínculos.
// La primera, segunda y ahora tercera sección mostrarán los encabezados de la primera sección.
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// Podemos desvincular el encabezado/pie de página de una sección anterior pasando "false" al llamar al método LinkToPrevious.
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

// También podemos seleccionar solo un tipo específico de encabezado/pie de página para vincular usando este método.
// La tercera sección ahora tendrá el mismo pie de página que la segunda y la primera sección, pero no el encabezado.
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// El encabezado/pie de página de la primera sección no puede vincularse a nada porque no existe una sección anterior.
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count);
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));

// Todos los encabezados/pies de página de la segunda sección están vinculados a los encabezados/pies de página de la primera sección.
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count);
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count(hf => ((HeaderFooter)hf).IsLinkedToPrevious));

// En la tercera sección, solo el pie de página está vinculado al pie de página de la primera sección a través de la segunda sección.
Assert.AreEqual(6, doc.Sections[2].HeadersFooters.Count);
Assert.AreEqual(5, doc.Sections[2].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));
Assert.True(doc.Sections[2].HeadersFooters[3].IsLinkedToPrevious);

doc.Save(ArtifactsDir + "HeaderFooter.Link.docx");
```

### Ver también

* class [Section](../../section/)
* class [HeaderFooter](../)
* espacio de nombres [Aspose.Words](../../headerfooter/)
* asamblea [Aspose.Words](../../../)


