---
title: HtmlSaveOptions.CssClassNamePrefix
linktitle: CssClassNamePrefix
articleTitle: CssClassNamePrefix
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية HtmlSaveOptions CssClassNamePrefix لتخصيص أسماء فئات CSS بسهولة باستخدام بادئة فريدة، مما يعزز اتساق تصميم الويب الخاص بك.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/htmlsaveoptions/cssclassnameprefix/
---
## HtmlSaveOptions.CssClassNamePrefix property

يحدد بادئة يتم إضافتها إلى جميع أسماء فئات CSS. القيمة الافتراضية هي سلسلة فارغة وأسماء فئات CSS المولدة لا تحتوي على بادئة مشتركة.

```csharp
public string CssClassNamePrefix { get; set; }
```

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentException | القيمة ليست فارغة وليست معرف CSS صالحًا. |

## ملاحظات

إذا لم تكن هذه القيمة فارغة، فستبدأ جميع فئات CSS التي تم إنشاؤها بواسطة Aspose.Words بالبادئة المحددة. قد يكون هذا مفيدًا، على سبيل المثال، إذا قمت بإضافة CSS مخصص إلى المستندات المولدة وتريد منع تعارضات اسم class .

إذا لم تكن القيمة`باطل` أو فارغًا، يجب أن يكون معرف CSS صالحًا.

## أمثلة

يوضح كيفية حفظ مستند بتنسيق HTML، وإضافة بادئة إلى جميع أسماء فئات CSS الخاصة به.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

HtmlSaveOptions saveOptions = new HtmlSaveOptions
{
    CssStyleSheetType = CssStyleSheetType.External,
    CssClassNamePrefix = "myprefix-"
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.CssClassNamePrefix.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.CssClassNamePrefix.html");

Assert.True(outDocContents.Contains("<p class=\"myprefix-Header\">"));
Assert.True(outDocContents.Contains("<p class=\"myprefix-Footer\">"));

outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.CssClassNamePrefix.css");

Assert.True(outDocContents.Contains(".myprefix-Footer { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:footer }"));
Assert.True(outDocContents.Contains(".myprefix-Header { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:header }"));
```

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
