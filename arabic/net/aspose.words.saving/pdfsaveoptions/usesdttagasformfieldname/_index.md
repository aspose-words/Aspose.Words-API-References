---
title: PdfSaveOptions.UseSdtTagAsFormFieldName
linktitle: UseSdtTagAsFormFieldName
articleTitle: UseSdtTagAsFormFieldName
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية PdfSaveOptions UseSdtTagAsFormFieldName على تحسين نماذج PDF من خلال استخدام علامات التحكم SDT لتحسين التنظيم والوضوح.
type: docs
weight: 340
url: /ar/net/aspose.words.saving/pdfsaveoptions/usesdttagasformfieldname/
---
## PdfSaveOptions.UseSdtTagAsFormFieldName property

يحدد ما إذا كان سيتم استخدام عنصر تحكم SDT Tag أو خاصية Id كاسم لحقل النموذج في PDF.

```csharp
public bool UseSdtTagAsFormFieldName { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`خطأ شنيع`.

عند ضبطه على`خطأ شنيع`يتم استخدام خاصية معرف عنصر التحكم SDT كاسم لحقل النموذج في PDF.

عند ضبطه على`حقيقي`يتم استخدام خاصية علامة التحكم SDT كاسم لحقل النموذج في PDF.

إذا تم ضبطه على`حقيقي` وإذا كان العلامة فارغة، فسيتم استخدام خاصية Id كاسم لحقل النموذج.

إذا تم ضبطه على`حقيقي` وقيم العلامة ليست فريدة، وسيتم تغيير قيم العلامة المكررة إلى أسماء حقول نموذج PDF فريدة build .

## أمثلة

يوضح كيفية استخدام عنصر التحكم SDT Tag أو Id كاسم لحقل النموذج في PDF.

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PreserveFormFields = true;
// عند تعيينه على 'false'، يتم استخدام خاصية معرف عنصر التحكم SDT كاسم لحقل النموذج في PDF.
// عند تعيينها على 'true'، يتم استخدام خاصية علامة عنصر التحكم SDT كاسم لحقل النموذج في PDF.
saveOptions.UseSdtTagAsFormFieldName = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.SdtTagAsFormFieldName.pdf", saveOptions);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
