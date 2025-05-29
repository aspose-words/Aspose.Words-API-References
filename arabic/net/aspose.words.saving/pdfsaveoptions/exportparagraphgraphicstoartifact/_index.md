---
title: PdfSaveOptions.ExportParagraphGraphicsToArtifact
linktitle: ExportParagraphGraphicsToArtifact
articleTitle: ExportParagraphGraphicsToArtifact
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ExportParagraphGraphicsToArtifact في PdfSaveOptions للتحكم في رسومات الفقرات كقطع أثرية، مما يعزز الوضوح البصري للمستند الخاص بك.
type: docs
weight: 160
url: /ar/net/aspose.words.saving/pdfsaveoptions/exportparagraphgraphicstoartifact/
---
## PdfSaveOptions.ExportParagraphGraphicsToArtifact property

يحصل على قيمة أو يعينها لتحديد ما إذا كان يجب وضع علامة على رسم فقرة كقطعة أثرية.

```csharp
public bool ExportParagraphGraphicsToArtifact { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`خطأ شنيع` وسيتم وضع علامة "Span" على الرسومات والفقرات (التسطير، وتأكيد النص، وما إلى ذلك) في البنية المنطقية للمستند.

عندما تكون القيمة`حقيقي` سيتم وضع علامة على رسومات الفقرة باعتبارها "قطعة أثرية".

يتم تجاهل هذه القيمة عند[`ExportDocumentStructure`](../exportdocumentstructure/) يكون`خطأ شنيع` .

## أمثلة

يوضح كيفية تصدير رسومات الفقرات كقطعة أثرية (التسطير، والتأكيد على النص، وما إلى ذلك).

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
