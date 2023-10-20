---
title: PdfSaveOptions.ExportParagraphGraphicsToArtifact
linktitle: ExportParagraphGraphicsToArtifact
articleTitle: ExportParagraphGraphicsToArtifact
second_title: Aspose.Words لـ .NET
description: PdfSaveOptions ExportParagraphGraphicsToArtifact ملكية. الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب وضع علامة على رسم الفقرة كقطعة أثرية في C#.
type: docs
weight: 160
url: /ar/net/aspose.words.saving/pdfsaveoptions/exportparagraphgraphicstoartifact/
---
## PdfSaveOptions.ExportParagraphGraphicsToArtifact property

الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب وضع علامة على رسم الفقرة كقطعة أثرية.

```csharp
public bool ExportParagraphGraphicsToArtifact { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`خطأ شنيع` ورسومات الفقرات (التسطير، إبراز النص، وما إلى ذلك) سيتم تمييزها على أنها "Span" في البنية المنطقية للمستند.

عندما تكون القيمة`حقيقي` سيتم وضع علامة على رسومات الفقرة على أنها "قطعة أثرية".

يتم تجاهل هذه القيمة عندما[`ExportDocumentStructure`](../exportdocumentstructure/) يكون`خطأ شنيع` .

## أمثلة

يوضح كيفية تصدير رسومات الفقرة كمنتج (تسطير، إبراز النص، وما إلى ذلك).

```csharp
Document doc = new Document(MyDir + "PDF artifacts.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.ExportDocumentStructure = true;
saveOptions.ExportParagraphGraphicsToArtifact = true;
saveOptions.TextCompression = PdfTextCompression.None;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportParagraphGraphicsToArtifact.pdf", saveOptions);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
