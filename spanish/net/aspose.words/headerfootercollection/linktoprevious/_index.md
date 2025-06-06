---
title: HeaderFooterCollection.LinkToPrevious
linktitle: LinkToPrevious
articleTitle: LinkToPrevious
second_title: Aspose.Words para .NET
description: Descubra el método LinkToPrevious en HeaderFooterCollection para conectar o desconectar fácilmente encabezados y pies de página en las secciones de su documento para lograr un formato perfecto.
type: docs
weight: 20
url: /es/net/aspose.words/headerfootercollection/linktoprevious/
---
## LinkToPrevious(*bool*) {#linktoprevious_1}

Vincula o desvincula todos los encabezados y pies de página a los encabezados y pies de página correspondientes en la sección anterior.

```csharp
public void LinkToPrevious(bool isLinkToPrevious)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| isLinkToPrevious | Boolean | `verdadero` para vincular los encabezados y pies de página a la sección anterior; `FALSO` para desvincularlos. |

## Observaciones

Si alguno de los encabezados o pies de página no existe, los crea automáticamente.

## Ejemplos

Muestra cómo vincular encabezados y pies de página entre secciones.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 3");

// Vaya a la primera sección y cree un encabezado y un pie de página. Por defecto,
// El encabezado y el pie de página solo aparecerán en las páginas de la sección que los contiene.
builder.MoveToSection(0);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header, which will be displayed in sections 1 and 2.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// Podemos vincular los encabezados/pies de página de una sección a los encabezados/pies de página de la sección anterior
// para permitir que la sección de enlace muestre los encabezados y pies de página de la sección vinculada.
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

Cada sección seguirá teniendo sus propios objetos de encabezado/pie de página. Al vincular secciones,
// la sección de enlace mostrará el encabezado y pie de página de la sección vinculada, conservando los suyos propios.
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// Vincula los encabezados/pies de página de la tercera sección con los encabezados/pies de página de la segunda sección.
// La segunda sección ya se vincula al encabezado/pie de página de la primera sección,
// Entonces, al vincularse a la segunda sección se creará una cadena de enlaces.
// La primera, segunda y ahora tercera sección mostrarán los encabezados de la primera sección.
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// Podemos desvincular el encabezado/pie de página de una sección anterior pasando "false" al llamar al método LinkToPrevious.
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

// También podemos seleccionar sólo un tipo específico de encabezado/pie de página para vincular usando este método.
// La tercera sección ahora tendrá el mismo pie de página que la segunda y la primera sección, pero no el encabezado.
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// El encabezado y pie de página de la primera sección no pueden vincularse a nada porque no hay una sección anterior.
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count);
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));

//Todos los encabezados y pies de página de la segunda sección están vinculados a los encabezados y pies de página de la primera sección.
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count);
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count(hf => ((HeaderFooter)hf).IsLinkedToPrevious));

// En la tercera sección, solo el pie de página está vinculado al pie de página de la primera sección a través de la segunda sección.
Assert.AreEqual(6, doc.Sections[2].HeadersFooters.Count);
Assert.AreEqual(5, doc.Sections[2].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));
Assert.True(doc.Sections[2].HeadersFooters[3].IsLinkedToPrevious);

doc.Save(ArtifactsDir + "HeaderFooter.Link.docx");
```

### Ver también

* class [HeaderFooterCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## LinkToPrevious(*[HeaderFooterType](../../headerfootertype/), bool*) {#linktoprevious}

Vincula o desvincula el encabezado o pie de página especificado con el encabezado o pie de página correspondiente en la sección anterior.

```csharp
public void LinkToPrevious(HeaderFooterType headerFooterType, bool isLinkToPrevious)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| headerFooterType | HeaderFooterType | A[`HeaderFooterType`](../../headerfootertype/) value que especifica el encabezado o pie de página a vincular/desvincular. |
| isLinkToPrevious | Boolean | `verdadero` para vincular el encabezado o pie de página a la sección anterior; `FALSO` Desvincular. |

## Observaciones

Si el encabezado o pie de página del tipo especificado no existe, lo crea automáticamente.

## Ejemplos

Muestra cómo vincular encabezados y pies de página entre secciones.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 3");

// Vaya a la primera sección y cree un encabezado y un pie de página. Por defecto,
// El encabezado y el pie de página solo aparecerán en las páginas de la sección que los contiene.
builder.MoveToSection(0);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header, which will be displayed in sections 1 and 2.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// Podemos vincular los encabezados/pies de página de una sección a los encabezados/pies de página de la sección anterior
// para permitir que la sección de enlace muestre los encabezados y pies de página de la sección vinculada.
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

Cada sección seguirá teniendo sus propios objetos de encabezado/pie de página. Al vincular secciones,
// la sección de enlace mostrará el encabezado y pie de página de la sección vinculada, conservando los suyos propios.
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// Vincula los encabezados/pies de página de la tercera sección con los encabezados/pies de página de la segunda sección.
// La segunda sección ya se vincula al encabezado/pie de página de la primera sección,
// Entonces, al vincularse a la segunda sección se creará una cadena de enlaces.
// La primera, segunda y ahora tercera sección mostrarán los encabezados de la primera sección.
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// Podemos desvincular el encabezado/pie de página de una sección anterior pasando "false" al llamar al método LinkToPrevious.
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

// También podemos seleccionar sólo un tipo específico de encabezado/pie de página para vincular usando este método.
// La tercera sección ahora tendrá el mismo pie de página que la segunda y la primera sección, pero no el encabezado.
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// El encabezado y pie de página de la primera sección no pueden vincularse a nada porque no hay una sección anterior.
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count);
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));

//Todos los encabezados y pies de página de la segunda sección están vinculados a los encabezados y pies de página de la primera sección.
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count);
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count(hf => ((HeaderFooter)hf).IsLinkedToPrevious));

// En la tercera sección, solo el pie de página está vinculado al pie de página de la primera sección a través de la segunda sección.
Assert.AreEqual(6, doc.Sections[2].HeadersFooters.Count);
Assert.AreEqual(5, doc.Sections[2].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));
Assert.True(doc.Sections[2].HeadersFooters[3].IsLinkedToPrevious);

doc.Save(ArtifactsDir + "HeaderFooter.Link.docx");
```

### Ver también

* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooterCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
