---
title: PageSet.All
linktitle: All
articleTitle: All
second_title: Aspose.Words para .NET
description: Acceda a todas las páginas del documento en su orden original con la propiedad "Conjunto de páginas". ¡Optimice su flujo de trabajo y mejore la gestión de documentos sin esfuerzo!
type: docs
weight: 20
url: /es/net/aspose.words.saving/pageset/all/
---
## PageSet.All property

Obtiene un conjunto con todas las páginas del documento en su orden original.

```csharp
public static PageSet All { get; }
```

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
