---
title: DocSaveOptions.AlwaysCompressMetafiles
linktitle: AlwaysCompressMetafiles
articleTitle: AlwaysCompressMetafiles
second_title: Aspose.Words para .NET
description: DocSaveOptions AlwaysCompressMetafiles propiedad. cuandoFALSO  los metarchivos pequeños no se comprimen por motivos de rendimiento. El valor predeterminado esverdadero  todos los metarchivos se comprimen independientemente de su tamaño en C#.
type: docs
weight: 20
url: /es/net/aspose.words.saving/docsaveoptions/alwayscompressmetafiles/
---
## DocSaveOptions.AlwaysCompressMetafiles property

cuando`FALSO` , los metarchivos pequeños no se comprimen por motivos de rendimiento. El valor predeterminado es`verdadero` , todos los metarchivos se comprimen independientemente de su tamaño.

```csharp
public bool AlwaysCompressMetafiles { get; set; }
```

## Ejemplos

Muestra cómo cambiar la compresión de metarchivos en un documento mientras se guarda.

```csharp
// Abra un documento que contenga una fórmula de Microsoft Equation 3.0.
Document doc = new Document(MyDir + "Microsoft equation object.docx");

// Cuando guardamos un documento, los metarchivos más pequeños no se comprimen por motivos de rendimiento.
// Podemos establecer una bandera en un objeto SaveOptions para comprimir cada metarchivo al guardar.
// Algunos editores como LibreOffice no pueden leer metarchivos sin comprimir.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.AlwaysCompressMetafiles = compressAllMetafiles;

doc.Save(ArtifactsDir + "DocSaveOptions.AlwaysCompressMetafiles.docx", saveOptions);

if (compressAllMetafiles)
    Assert.That(10000, Is.LessThan(new FileInfo(ArtifactsDir + "DocSaveOptions.AlwaysCompressMetafiles.docx").Length));
else
    Assert.That(30000, Is.AtLeast(new FileInfo(ArtifactsDir + "DocSaveOptions.AlwaysCompressMetafiles.docx").Length));
```

### Ver también

* class [DocSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
