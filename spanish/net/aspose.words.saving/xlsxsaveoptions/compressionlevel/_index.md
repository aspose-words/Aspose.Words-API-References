---
title: XlsxSaveOptions.CompressionLevel
second_title: Referencia de API de Aspose.Words para .NET
description: XlsxSaveOptions propiedad. Especifica el nivel de compresión utilizado para guardar el documento. El valor predeterminado esNormal .
type: docs
weight: 20
url: /es/net/aspose.words.saving/xlsxsaveoptions/compressionlevel/
---
## XlsxSaveOptions.CompressionLevel property

Especifica el nivel de compresión utilizado para guardar el documento. El valor predeterminado esNormal .

```csharp
public CompressionLevel CompressionLevel { get; set; }
```

### Ejemplos

Muestra cómo comprimir un documento XLSX.

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
xlsxSaveOptions.CompressionLevel = CompressionLevel.Maximum; 

doc.Save(ArtifactsDir + "XlsxSaveOptions.CompressXlsx.xlsx", xlsxSaveOptions);
```

### Ver también

* enum [CompressionLevel](../../compressionlevel/)
* class [XlsxSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../xlsxsaveoptions/)
* asamblea [Aspose.Words](../../../)


