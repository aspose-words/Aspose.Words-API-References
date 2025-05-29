---
title: XlsxSaveOptions.CompressionLevel
linktitle: CompressionLevel
articleTitle: CompressionLevel
second_title: Aspose.Words für .NET
description: Entdecken Sie die XlsxSaveOptions CompressionLevel-Eigenschaft, um das Speichern von Dokumenten mit anpassbaren Komprimierungseinstellungen für eine effiziente Dateiverwaltung zu optimieren.
type: docs
weight: 20
url: /de/net/aspose.words.saving/xlsxsaveoptions/compressionlevel/
---
## XlsxSaveOptions.CompressionLevel property

Gibt die Komprimierungsstufe an, die zum Speichern des Dokuments verwendet wird. Der Standardwert istNormal .

```csharp
public CompressionLevel CompressionLevel { get; set; }
```

## Beispiele

Zeigt, wie ein XLSX-Dokument komprimiert wird.

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
xlsxSaveOptions.CompressionLevel = CompressionLevel.Maximum;
xlsxSaveOptions.SaveFormat = SaveFormat.Xlsx;

doc.Save(ArtifactsDir + "XlsxSaveOptions.CompressXlsx.xlsx", xlsxSaveOptions);
```

### Siehe auch

* enum [CompressionLevel](../../compressionlevel/)
* class [XlsxSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
