---
title: BlockImportMode Enum
linktitle: BlockImportMode
articleTitle: BlockImportMode
second_title: Aspose.Words para .NET
description: Descubra cómo la enumeración Aspose.Words.BlockImportMode mejora la integración de documentos HTML al optimizar las importaciones de propiedades de elementos a nivel de bloque para flujos de trabajo fluidos.
type: docs
weight: 4010
url: /es/net/aspose.words.loading/blockimportmode/
---
## BlockImportMode enumeration

Especifica cómo se importan las propiedades de los elementos a nivel de bloque desde documentos basados en HTML.

```csharp
public enum BlockImportMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Merge | `0` | Las propiedades de los bloques principales se fusionan y almacenan en elementos secundarios (es decir, párrafos o tablas). |
| Preserve | `1` | Las propiedades de los bloques principales se importan a una estructura lógica especial y se almacenan por separado de los nodos del documento. |

## Ejemplos

Muestra cómo se importan las propiedades de los elementos a nivel de bloque desde documentos basados en HTML.

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
MemoryStream stream = new MemoryStream(Encoding.UTF8.GetBytes(html));

HtmlLoadOptions loadOptions = new HtmlLoadOptions();
// Establezca el nuevo modo de importación de elementos a nivel de bloque HTML.
loadOptions.BlockImportMode = blockImportMode;

Document doc = new Document(stream, loadOptions);
doc.Save(ArtifactsDir + "HtmlLoadOptions.BlockImport.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Loading](../../aspose.words.loading/)
* asamblea [Aspose.Words](../../)
