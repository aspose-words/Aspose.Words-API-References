---
title: HeaderFooterType Enum
linktitle: HeaderFooterType
articleTitle: HeaderFooterType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.HeaderFooterType para identificar fácilmente los tipos de encabezado y pie de página en documentos de Word. ¡Mejore su gestión de documentos hoy mismo!
type: docs
weight: 3550
url: /es/net/aspose.words/headerfootertype/
---
## HeaderFooterType enumeration

Identifica el tipo de encabezado o pie de página que se encuentra en un archivo de Word.

```csharp
public enum HeaderFooterType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| HeaderEven | `0` | Encabezado para páginas pares. |
| HeaderPrimary | `1` | Encabezado principal, también se utiliza para páginas impares. |
| FooterEven | `2` | Pie de página para páginas pares. |
| FooterPrimary | `3` | Pie de página principal, también se utiliza para páginas impares. |
| HeaderFirst | `4` | Encabezado para la primera página de la sección. |
| FooterFirst | `5` | Pie de página para la primera página de la sección. |

## Ejemplos

Muestra cómo crear encabezados y pies de página en un documento utilizando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Especificamos que queremos encabezados y pies de página diferentes para la primera página, páginas pares e impares.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Cree los encabezados y luego agregue tres páginas al documento para mostrar cada tipo de encabezado.
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

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
