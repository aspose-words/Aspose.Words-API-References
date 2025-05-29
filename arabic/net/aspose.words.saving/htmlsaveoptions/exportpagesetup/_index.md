---
title: HtmlSaveOptions.ExportPageSetup
linktitle: ExportPageSetup
articleTitle: ExportPageSetup
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية HtmlSaveOptions ExportPageSetup على تعزيز صادرات HTML أو MHTML أو EPUB من خلال السماح بإعدادات صفحة قابلة للتخصيص للحصول على إخراج أفضل.
type: docs
weight: 220
url: /ar/net/aspose.words.saving/htmlsaveoptions/exportpagesetup/
---
## HtmlSaveOptions.ExportPageSetup property

يحدد ما إذا كان سيتم تصدير إعداد الصفحة إلى HTML أو MHTML أو EPUB. الافتراضي هو`خطأ شنيع` .

```csharp
public bool ExportPageSetup { get; set; }
```

## ملاحظات

كل[`Section`](../../../aspose.words/section/) في نموذج مستند Aspose.Words يوفر معلومات إعداد الصفحة عبر[`PageSetup`](../../../aspose.words/pagesetup/) عند تصدير مستند بتنسيق HTML، قد تحتاج إلى الاحتفاظ بهذه المعلومات لاستخدامها لاحقًا. على وجه الخصوص، قد يكون إعداد الصفحة مهمًا لعرضها على وسائط مقسمة إلى صفحات (طباعة) أو التحويل اللاحق إلى تنسيقات ملفات Microsoft Word الأصلية (DOCX، DOC، RTF، WML).

في أغلب الأحيان، يُقصد بـ HTML عرض الصفحات في المتصفحات التي لا تُطبّق الترقيم. لذا، تكون هذه الخاصية غير نشطة افتراضيًا.

## أمثلة

يوضح كيفية تحديد ما إذا كان سيتم الحفاظ على معلومات هيكل القسم/إعداد الصفحة عند الحفظ في HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TopMargin = 36.0;
pageSetup.BottomMargin = 36.0;
pageSetup.PaperSize = PaperSize.A5;

// عند حفظ المستند في HTML، يمكننا تمرير كائن SaveOptions
// لتحديد ما إذا كان سيتم الحفاظ على إعدادات إعداد الصفحة أو تجاهلها.
// إذا قمنا بتعيين علامة "ExportPageSetup" إلى "true"، فسوف تحتوي وثيقة HTML الناتجة على تكوين إعداد الصفحة الخاص بنا.
// إذا قمنا بتعيين علامة "ExportPageSetup" إلى "false"، فإن عملية الحفظ ستتجاهل إعدادات إعداد الصفحة الخاصة بنا
// بالنسبة للقسم الأول، وسوف يبدو كلا القسمين متطابقين.
HtmlSaveOptions options = new HtmlSaveOptions { ExportPageSetup = exportPageSetup };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportPageSetup.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportPageSetup.html");

if (exportPageSetup)
{
    Assert.True(outDocContents.Contains(
        "<style type=\"text/css\">" +
            "@page Section_1 { size:419.55pt 595.3pt; margin:36pt 70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" +
            "@page Section_2 { size:612pt 792pt; margin:70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" +
            "div.Section_1 { page:Section_1 }div.Section_2 { page:Section_2 }" +
        "</style>"));

    Assert.True(outDocContents.Contains(
        "<div class=\"Section_1\">" +
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<span>Section 1</span>" +
            "</p>" +
        "</div>"));
}
else
{
    Assert.False(outDocContents.Contains("style type=\"text/css\">"));

    Assert.True(outDocContents.Contains(
        "<div>" +
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<span>Section 1</span>" +
            "</p>" +
        "</div>"));
}
```

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
