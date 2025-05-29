---
title: PageSet.Even
linktitle: Even
articleTitle: Even
second_title: Aspose.Words para .NET
description: Recupere un conjunto de todas las páginas pares de su documento en su orden original con PageSet Even. ¡Optimice su flujo de trabajo y mejore la gestión de documentos!
type: docs
weight: 30
url: /es/net/aspose.words.saving/pageset/even/
---
## PageSet.Even property

Obtiene un conjunto con todas las páginas pares del documento en su orden original.

```csharp
public static PageSet Even { get; }
```

## Observaciones

Las páginas pares tienen índices impares, ya que los índices de página se basan en cero.

## Ejemplos

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

* class [PageSet](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
