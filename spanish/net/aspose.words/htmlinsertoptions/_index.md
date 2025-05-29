---
title: HtmlInsertOptions Enum
linktitle: HtmlInsertOptions
articleTitle: HtmlInsertOptions
second_title: Aspose.Words para .NET
description: Explore la enumeración Aspose.Words.HtmlInsertOptions para personalizar la inserción de HTML con el método InsertHtml, mejorando la eficiencia del procesamiento de documentos.
type: docs
weight: 3570
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
| UseBuilderFormatting | `1` | Utilice la fuente y el formato de párrafo especificados en[`DocumentBuilder`](../documentbuilder/) como formato base para el texto insertado desde HTML. |
| RemoveLastEmptyParagraph | `2` | Elimina el párrafo vacío que normalmente se inserta después del HTML que termina con un elemento de nivel de bloque. |
| PreserveBlocks | `4` | Conservar las propiedades de los elementos a nivel de bloque. |

## Ejemplos

Muestra cómo se pueden conservar mejor los bordes y márgenes visibles.

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

// Establezca el nuevo modo de importación de elementos a nivel de bloque HTML.
HtmlInsertOptions insertOptions = HtmlInsertOptions.PreserveBlocks;

DocumentBuilder builder = new DocumentBuilder();
builder.InsertHtml(html, insertOptions);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.PreserveBlocks.docx");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
