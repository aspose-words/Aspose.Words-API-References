---
title: HtmlSaveOptions.ExportTextInputFormFieldAsText
linktitle: ExportTextInputFormFieldAsText
articleTitle: ExportTextInputFormFieldAsText
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية HtmlSaveOptions ExportTextInputFormFieldAsText حقول نموذج إدخال النص لحفظ HTML أو MHTML بسلاسة. حسّن عملية التصدير!
type: docs
weight: 260
url: /ar/net/aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext/
---
## HtmlSaveOptions.ExportTextInputFormFieldAsText property

يتحكم في كيفية حفظ حقول نموذج إدخال النص في HTML أو MHTML. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool ExportTextInputFormFieldAsText { get; set; }
```

## ملاحظات

عند ضبطه على`حقيقي` ، يصدر حقول نموذج إدخال النص كنص عادي. عندما`خطأ شنيع`، يصدر حقول نموذج إدخال النص Word كعناصر INPUT في HTML.

عند التصدير إلى EPUB، يتم دائمًا حفظ حقول نموذج إدخال النص كنص due وفقًا لمتطلبات هذا التنسيق.

## أمثلة

يوضح كيفية تحديد المجلد لتخزين الصور المرتبطة بعد حفظها في .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// تعيين خيار لتصدير حقول النموذج كنص عادي بدلاً من عناصر إدخال HTML.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
