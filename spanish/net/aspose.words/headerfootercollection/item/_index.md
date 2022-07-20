---
title: Item
second_title: Referencia de API de Aspose.Words para .NET
description: Recupera un EncabezadoPie de página en el índice dado.
type: docs
weight: 10
url: /es/net/aspose.words/headerfootercollection/item/
---
## HeaderFooterCollection indexer (1 of 2)

Recupera un **EncabezadoPie de página** en el índice dado.

```csharp
public HeaderFooter this[int index] { get; }
```

| Parámetro | Descripción |
| --- | --- |
| index | Un índice de la colección. |

### Observaciones

El índice está basado en cero.

Los índices negativos están permitidos e indican el acceso desde la parte posterior de la colección. Por ejemplo, -1 significa el último elemento, -2 significa el penúltimo y así sucesivamente.

Si el índice es mayor o igual que el número de elementos en la lista, esto devuelve una referencia nula.

Si el índice es negativo y su valor absoluto es mayor que el número de elementos de la lista, esto devuelve una referencia nula.

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

// Vaya a la primera sección y cree un encabezado y un pie de página. Por defecto,
// el encabezado y el pie de página solo aparecerán en las páginas de la sección que los contiene.
builder.MoveToSection(0);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header, which will be displayed in sections 1 and 2.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// Podemos vincular los encabezados/pies de página de una sección a los encabezados/pies de página de la sección anterior
// para permitir que la sección de enlace muestre los encabezados/pies de página de la sección enlazada.
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

// Cada sección aún tendrá sus propios objetos de encabezado/pie de página. Cuando vinculamos secciones,
// la sección de enlace mostrará el encabezado/pie de página de la sección enlazada manteniendo el suyo propio.
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// Vincular los encabezados/pies de página de la tercera sección a los encabezados/pies de página de la segunda sección.
// La segunda sección ya enlaza con el encabezado/pie de página de la primera sección,
// por lo que vincular a la segunda sección creará una cadena de enlaces.
// La primera, la segunda y ahora la tercera sección mostrarán los encabezados de la primera sección.
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// Podemos desvincular el encabezado/pie de página de una sección anterior pasando "falso" al llamar al método LinkToPrevious.
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

// También podemos seleccionar solo un tipo específico de encabezado/pie de página para vincular usando este método.
// La tercera sección ahora tendrá el mismo pie de página que la segunda y la primera sección, pero no el encabezado.
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// Los encabezados/pies de página de la primera sección no pueden vincularse a nada porque no hay una sección anterior.
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

* class [HeaderFooter](../../headerfooter)
* class [HeaderFooterCollection](../../headerfootercollection)
* espacio de nombres [Aspose.Words](../../headerfootercollection)
* asamblea [Aspose.Words](../../../)

---

## HeaderFooterCollection indexer (2 of 2)

Recupera un **EncabezadoPie de página** del tipo especificado.

```csharp
public HeaderFooter this[HeaderFooterType headerFooterType] { get; }
```

| Parámetro | Descripción |
| --- | --- |
| headerFooterType | A[`HeaderFooterType`](../../headerfootertype) value que especifica el tipo de encabezado/pie de página a recuperar. |

### Observaciones

Devuelve nulo si no se encuentra el encabezado/pie de página del tipo especificado.

### Ejemplos

Muestra cómo reemplazar texto en el pie de página de un documento.

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

Muestra cómo eliminar todos los pies de página de un documento.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Iterar a través de cada sección y eliminar pies de página de todo tipo.
foreach (Section section in doc.OfType<Section>())
{
    // Hay tres tipos de tipos de encabezado y pie de página.
    // 1 - El encabezado/pie de página "Primero", que solo aparece en la primera página de una sección.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 - El encabezado/pie de página "Principal", que aparece en las páginas impares.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

      // 3 - El encabezado/pie de página "Even", que aparece en las páginas pares.
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

### Ver también

* class [HeaderFooter](../../headerfooter)
* enum [HeaderFooterType](../../headerfootertype)
* class [HeaderFooterCollection](../../headerfootercollection)
* espacio de nombres [Aspose.Words](../../headerfootercollection)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
