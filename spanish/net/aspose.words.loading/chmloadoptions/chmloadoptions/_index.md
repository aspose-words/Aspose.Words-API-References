---
title: ChmLoadOptions
linktitle: ChmLoadOptions
articleTitle: ChmLoadOptions
second_title: Aspose.Words para .NET
description: Descubra el constructor ChmLoadOptions para una inicialización fluida. Establezca valores predeterminados fácilmente y mejore el rendimiento de su aplicación hoy mismo.
type: docs
weight: 10
url: /es/net/aspose.words.loading/chmloadoptions/chmloadoptions/
---
## ChmLoadOptions constructor

Inicializa una nueva instancia de esta clase con valores predeterminados.

```csharp
public ChmLoadOptions()
```

## Ejemplos

Muestra cómo resolver URL como "ms-its:myfile.chm::/index.htm".

```csharp
// Nuestro documento contiene URL como "ms-its:amhelp.chm::....htm", pero tiene un nombre diferente,
// Entonces los enlaces de archivos no funcionan después de guardarlos en HTML.
// Necesitamos definir el nombre del archivo original en 'ChmLoadOptions' para evitar este comportamiento.
ChmLoadOptions loadOptions = new ChmLoadOptions { OriginalFileName = "amhelp.chm" };

Document doc = new Document(new MemoryStream(File.ReadAllBytes(MyDir + "Document with ms-its links.chm")),
    loadOptions);

doc.Save(ArtifactsDir + "ExChmLoadOptions.OriginalFileName.html");
```

### Ver también

* class [ChmLoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
