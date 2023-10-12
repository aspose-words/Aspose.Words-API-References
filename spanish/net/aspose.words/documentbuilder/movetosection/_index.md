---
title: DocumentBuilder.MoveToSection
second_title: Referencia de API de Aspose.Words para .NET
description: DocumentBuilder método. Mueve el cursor al principio del cuerpo en una sección especificada.
type: docs
weight: 580
url: /es/net/aspose.words/documentbuilder/movetosection/
---
## DocumentBuilder.MoveToSection method

Mueve el cursor al principio del cuerpo en una sección especificada.

```csharp
public void MoveToSection(int sectionIndex)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| sectionIndex | Int32 | El índice de la sección a la que pasar. |

### Observaciones

Cuando*sectionIndex* es mayor o igual a 0, especifica un índice desde el comienzo del documento siendo 0 la primera sección. Cuando*sectionIndex* es menor que 0, , especificó un índice desde el final del documento, siendo -1 la última sección.

El cursor se mueve al primer párrafo del[`Body`](../../body/) de la sección especificada.

### Ejemplos

Muestra cómo crear encabezados y pies de página en un documento usando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Especifica que queremos encabezados y pies de página diferentes para las primeras páginas, pares e impares.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Cree los encabezados, luego agregue tres páginas al documento para mostrar cada tipo de encabezado.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

### Ver también

* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)


