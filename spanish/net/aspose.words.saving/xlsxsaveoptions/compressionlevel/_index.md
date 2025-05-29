---
title: XlsxSaveOptions.CompressionLevel
linktitle: CompressionLevel
articleTitle: CompressionLevel
second_title: Aspose.Words para .NET
description: Descubra la propiedad CompressionLevel de XlsxSaveOptions para optimizar el guardado de documentos con configuraciones de compresión personalizables para una gestión eficiente de archivos.
type: docs
weight: 20
url: /es/net/aspose.words.saving/xlsxsaveoptions/compressionlevel/
---
## XlsxSaveOptions.CompressionLevel property

Especifica el nivel de compresión utilizado para guardar el documento. El valor predeterminado esNormal .

```csharp
public CompressionLevel CompressionLevel { get; set; }
```

## Ejemplos

Muestra cómo comprimir documentos XLSX.

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
xlsxSaveOptions.CompressionLevel = CompressionLevel.Maximum;
xlsxSaveOptions.SaveFormat = SaveFormat.Xlsx;

doc.Save(ArtifactsDir + "XlsxSaveOptions.CompressXlsx.xlsx", xlsxSaveOptions);
```

### Ver también

* enum [CompressionLevel](../../compressionlevel/)
* class [XlsxSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
