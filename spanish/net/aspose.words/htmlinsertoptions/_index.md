---
title: HtmlInsertOptions Enum
linktitle: HtmlInsertOptions
articleTitle: HtmlInsertOptions
second_title: Aspose.Words para .NET
description: Aspose.Words.HtmlInsertOptions enumeración. Especifica opciones para elInsertHtml método en C#.
type: docs
weight: 3140
url: /es/net/aspose.words/htmlinsertoptions/
---
## HtmlInsertOptions enumeration

Especifica opciones para el[`InsertHtml`](../documentbuilder/inserthtml/) método.

```csharp
[Flags]
public enum HtmlInsertOptions
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | Utilice las opciones predeterminadas al insertar HTML. |
| UseBuilderFormatting | `1` | Utilice el formato de fuente y párrafo especificado en[`DocumentBuilder`](../documentbuilder/) como formato base para text insertado desde HTML. |
| RemoveLastEmptyParagraph | `2` | Elimina el párrafo vacío que normalmente se inserta después del HTML y que termina con un elemento a nivel de bloque. |
| PreserveBlocks | `4` | Preservar las propiedades de los elementos a nivel de bloque. |

## Ejemplos

Muestra cómo permite preservar mejor los bordes y márgenes vistos.

```csharp
const string html = @"
    <html>
        <div style='border:dotted'>
        <div style='border:solid'>
            <p>paragraph 1</p>
            <p>paragraph 2</p>
        </div>
        </div>
    </html>";

// Establece el nuevo modo de importar elementos HTML a nivel de bloque.
HtmlInsertOptions insertOptions = HtmlInsertOptions.PreserveBlocks;

DocumentBuilder builder = new DocumentBuilder();
builder.InsertHtml(html, insertOptions);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.PreserveBlocks.docx");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
