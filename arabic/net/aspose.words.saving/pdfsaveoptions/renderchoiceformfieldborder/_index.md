---
title: PdfSaveOptions.RenderChoiceFormFieldBorder
linktitle: RenderChoiceFormFieldBorder
articleTitle: RenderChoiceFormFieldBorder
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية PdfSaveOptions RenderChoiceFormFieldBorder على تعزيز تصميم نموذج PDF من خلال التحكم في حدود حقل الاختيار لتحقيق تجربة مستخدم أفضل.
type: docs
weight: 290
url: /ar/net/aspose.words.saving/pdfsaveoptions/renderchoiceformfieldborder/
---
## PdfSaveOptions.RenderChoiceFormFieldBorder property

يحدد ما إذا كان سيتم عرض حدود حقل نموذج اختيار PDF.

```csharp
public bool RenderChoiceFormFieldBorder { get; set; }
```

## ملاحظات

يتم استخدام حقول نموذج اختيار PDF لتصدير عنصر التحكم في محتوى مربع التحرير والسرد SDT وعنصر التحكم في قائمة SDT المنسدلة Content وحقل النموذج المنسدل القديم عندما[`PreserveFormFields`](../preserveformfields/) تم تمكين الخيار.

القيمة الافتراضية هي`حقيقي`.

## أمثلة

يوضح كيفية عرض حدود حقل نموذج اختيار PDF.

```csharp
Document doc = new Document(MyDir + "Legacy drop-down.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PreserveFormFields = true;
saveOptions.RenderChoiceFormFieldBorder = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderChoiceFormFieldBorder.pdf", saveOptions);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
