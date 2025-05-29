---
title: XlsxSaveOptions.CompressionLevel
linktitle: CompressionLevel
articleTitle: CompressionLevel
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية CompressionLevel في XlsxSaveOptions لتحسين حفظ المستندات باستخدام إعدادات الضغط القابلة للتخصيص لإدارة الملفات بكفاءة.
type: docs
weight: 20
url: /ar/net/aspose.words.saving/xlsxsaveoptions/compressionlevel/
---
## XlsxSaveOptions.CompressionLevel property

يحدد مستوى الضغط المستخدم لحفظ المستند. القيمة الافتراضية هيNormal .

```csharp
public CompressionLevel CompressionLevel { get; set; }
```

## أمثلة

يوضح كيفية ضغط مستند XLSX.

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
xlsxSaveOptions.CompressionLevel = CompressionLevel.Maximum;
xlsxSaveOptions.SaveFormat = SaveFormat.Xlsx;

doc.Save(ArtifactsDir + "XlsxSaveOptions.CompressXlsx.xlsx", xlsxSaveOptions);
```

### أنظر أيضا

* enum [CompressionLevel](../../compressionlevel/)
* class [XlsxSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
