---
title: FixedPageSaveOptions.PageSet
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words para .NET
description: Controla la renderización de tus documentos con FixedPageSaveOptions PageSet. Selecciona fácilmente páginas específicas o elige todas para una salida fluida. ¡Optimiza tu flujo de trabajo!
type: docs
weight: 70
url: /es/net/aspose.words.saving/fixedpagesaveoptions/pageset/
---
## FixedPageSaveOptions.PageSet property

Obtiene o establece las páginas que se representarán. El valor predeterminado son todas las páginas del documento.

```csharp
public PageSet PageSet { get; set; }
```

## Ejemplos

Muestra cómo extraer páginas basándose en índices de página exactos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//Añadir cinco páginas al documento.
for (int i = 1; i < 6; i++)
{
    builder.Write("Page " + i);
    builder.InsertBreak(BreakType.PageBreak);
}

// Crea un objeto "XpsSaveOptions", que podemos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// Utilice la propiedad "PageSet" para seleccionar un conjunto de páginas del documento para guardar en la salida XPS.
// En este caso, elegiremos, mediante un índice basado en cero, solo tres páginas: página 1, página 2 y página 4.
xpsOptions.PageSet = new PageSet(0, 1, 3);

doc.Save(ArtifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

Muestra cómo convertir solo algunas de las páginas de un documento a PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

using (Stream stream = File.Create(ArtifactsDir + "PdfSaveOptions.OnePage.pdf"))
{
    // Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
    // para modificar la forma en que ese método convierte el documento a .PDF.
    PdfSaveOptions options = new PdfSaveOptions();

    // Establezca "PageIndex" en "1" para representar una parte del documento a partir de la segunda página.
    options.PageSet = new PageSet(1);

    //Este documento contendrá una página a partir de la página dos, que solo contendrá la segunda página.
    doc.Save(stream, options);
}
```

Muestra cómo exportar páginas impares del documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 5; i++)
{
    builder.Writeln($"Page {i + 1} ({(i % 2 == 0 ? "odd" : "even")})");
    if (i < 4)
        builder.InsertBreak(BreakType.PageBreak);
}

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// A continuación se muestran tres propiedades de PageSet que podemos usar para filtrar un conjunto de páginas.
// nuestro documento para guardar en un documento PDF de salida en función de la paridad de sus números de página.
// 1 - Guardar sólo las páginas pares:
options.PageSet = PageSet.Even;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.Even.pdf", options);

// 2 - Guardar sólo las páginas impares:
options.PageSet = PageSet.Odd;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.Odd.pdf", options);

// 3 - Guardar cada página:
options.PageSet = PageSet.All;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.All.pdf", options);
```

### Ver también

* class [PageSet](../../pageset/)
* class [FixedPageSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
