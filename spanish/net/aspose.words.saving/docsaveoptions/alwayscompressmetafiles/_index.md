---
title: DocSaveOptions.AlwaysCompressMetafiles
linktitle: AlwaysCompressMetafiles
articleTitle: AlwaysCompressMetafiles
second_title: Aspose.Words para .NET
description: Optimice la gestión de documentos con la propiedad AlwaysCompressMetafiles. Mejore el rendimiento controlando la compresión de metarchivos para mayor eficiencia.
type: docs
weight: 20
url: /es/net/aspose.words.saving/docsaveoptions/alwayscompressmetafiles/
---
## DocSaveOptions.AlwaysCompressMetafiles property

Cuando`FALSO` Los metarchivos pequeños no se comprimen por razones de rendimiento. El valor predeterminado es`verdadero` , todos los metarchivos se comprimen independientemente de su tamaño.

```csharp
public bool AlwaysCompressMetafiles { get; set; }
```

## Ejemplos

Muestra cómo cambiar la compresión de metarchivos en un documento mientras se guarda.

```csharp
//Abra un documento que contenga una fórmula de Microsoft Equation 3.0.
Document doc = new Document(MyDir + "Microsoft equation object.docx");

// Cuando guardamos un documento, los metarchivos más pequeños no se comprimen por razones de rendimiento.
//Podemos establecer una bandera en un objeto SaveOptions para comprimir cada metarchivo al guardar.
//Algunos editores como LibreOffice no pueden leer metarchivos sin comprimir.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.AlwaysCompressMetafiles = compressAllMetafiles;

doc.Save(ArtifactsDir + "DocSaveOptions.AlwaysCompressMetafiles.docx", saveOptions);
```

### Ver también

* class [DocSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
