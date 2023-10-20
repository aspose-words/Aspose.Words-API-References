---
title: HtmlSaveOptions.CssClassNamePrefix
linktitle: CssClassNamePrefix
articleTitle: CssClassNamePrefix
second_title: Aspose.Words لـ .NET
description: HtmlSaveOptions CssClassNamePrefix ملكية. تحديد بادئة تتم إضافتها إلى كافة أسماء فئات CSS. القيمة الافتراضية هي سلسلة فارغة وأسماء فئات CSS التي تم إنشاؤها لا تحتوي على بادئة مشتركة في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/htmlsaveoptions/cssclassnameprefix/
---
## HtmlSaveOptions.CssClassNamePrefix property

تحديد بادئة تتم إضافتها إلى كافة أسماء فئات CSS. القيمة الافتراضية هي سلسلة فارغة وأسماء فئات CSS التي تم إنشاؤها لا تحتوي على بادئة مشتركة.

```csharp
public string CssClassNamePrefix { get; set; }
```

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentException | القيمة ليست فارغة وليست معرف CSS صالحًا. |

## ملاحظات

إذا لم تكن هذه القيمة فارغة، فستبدأ جميع فئات CSS التي تم إنشاؤها بواسطة Aspose.Words بالبادئة المحددة. قد يكون هذا مفيدًا، على سبيل المثال، إذا قمت بإضافة CSS مخصص إلى المستندات التي تم إنشاؤها وتريد منع تعارض أسماء class .

إذا كانت القيمة ليست كذلك`باطل` أو فارغًا، يجب أن يكون معرف CSS صالحًا.

## أمثلة

يوضح كيفية حفظ مستند إلى HTML، وإضافة بادئة لجميع أسماء فئات CSS الخاصة به.

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

Assert.True(outDocContents.Contains(".myprefix-Footer { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt }\r\n" +
                                    ".myprefix-Header { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt }\r\n"));
```

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
