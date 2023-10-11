---
title: HtmlLoadOptions.BlockImportMode
second_title: Referencia de API de Aspose.Words para .NET
description: HtmlLoadOptions propiedad. Obtiene o establece un valor que especifica cómo se importan las propiedades de los elementos a nivel de bloque. El valor predeterminado esMerge .
type: docs
weight: 20
url: /es/net/aspose.words.loading/htmlloadoptions/blockimportmode/
---
## HtmlLoadOptions.BlockImportMode property

Obtiene o establece un valor que especifica cómo se importan las propiedades de los elementos a nivel de bloque. El valor predeterminado esMerge .

```csharp
public BlockImportMode BlockImportMode { get; set; }
```

### Ejemplos

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
// Establece el nuevo modo de importar elementos HTML a nivel de bloque.
loadOptions.BlockImportMode = blockImportMode;

Document doc = new Document(stream, loadOptions);
doc.Save(ArtifactsDir + "HtmlLoadOptions.BlockImport.docx");
```

### Ver también

* enum [BlockImportMode](../../blockimportmode/)
* class [HtmlLoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../htmlloadoptions/)
* asamblea [Aspose.Words](../../../)


