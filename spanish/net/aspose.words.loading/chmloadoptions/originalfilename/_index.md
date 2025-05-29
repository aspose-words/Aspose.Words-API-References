---
title: ChmLoadOptions.OriginalFileName
linktitle: OriginalFileName
articleTitle: OriginalFileName
second_title: Aspose.Words para .NET
description: Descubra la propiedad ChmLoadOptions OriginalFileName y configure fácilmente el nombre del archivo CHM para un acceso optimizado. El valor predeterminado es nulo. ¡Optimice su experiencia!
type: docs
weight: 20
url: /es/net/aspose.words.loading/chmloadoptions/originalfilename/
---
## ChmLoadOptions.OriginalFileName property

El nombre del archivo CHM. El valor predeterminado es`nulo` .

```csharp
public string OriginalFileName { get; set; }
```

## Observaciones

Los documentos CHM pueden contener enlaces que hacen referencia al mismo documento por nombre de archivo. Aspose.Words admite dichos enlaces y normalmente utiliza[`OriginalFileName`](../../../aspose.words/document/originalfilename/) Para comprobar si el archivo referenciado por un enlace es el archivo que se está cargando. Si un documento se carga desde una secuencia, su nombre de archivo original debe especificarse explícitamente mediante esta propiedad, ya que no se puede determinar automáticamente.

Si se carga un documento CHM desde un archivo y se especifica un valor distinto de nulo para esta propiedad, el valor tendrá prioridad sobre el nombre real del archivo almacenado en él.[`OriginalFileName`](../../../aspose.words/document/originalfilename/) .

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
