---
title: HtmlFixedSaveOptions.SaveFontFaceCssSeparately
linktitle: SaveFontFaceCssSeparately
articleTitle: SaveFontFaceCssSeparately
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية SaveFontFaceCssSeparately على تحسين إدارة CSS للمستند الخاص بك عن طريق حفظ قواعد وجه الخط في ملف منفصل للحصول على صادرات أنظف.
type: docs
weight: 180
url: /ar/net/aspose.words.saving/htmlfixedsaveoptions/savefontfacecssseparately/
---
## HtmlFixedSaveOptions.SaveFontFaceCssSeparately property

يشير العلم إلى ما إذا كان يجب وضع قواعد CSS "@font-face" في ملف منفصل "fontFaces.css" عند حفظ مستند باستخدام جدول أنماط خارجي (أي عندما[`ExportEmbeddedCss`](../exportembeddedcss/) هو`خطأ شنيع` ). القيمة الافتراضية هي`خطأ شنيع` ، تتم كتابة جميع قواعد CSS في ملف واحد "styles.css".

```csharp
public bool SaveFontFaceCssSeparately { get; set; }
```

## ملاحظات

تعيين هذه الخاصية إلى`حقيقي` يستعيد السلوك القديم (ملفات منفصلة) للتوافق مع الكود القديم.

## أمثلة

يوضح كيفية وضع CSS في ملف منفصل وإضافة بادئة إلى جميع أسماء فئات CSS الخاصة به.

```csharp
Document doc = new Document(MyDir + "Bookmarks.docx");

HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    CssClassNamesPrefix = "myprefix",
    SaveFontFaceCssSeparately = true
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix.html");

Assert.True(Regex.Match(outDocContents,
    "<div class=\"myprefixdiv myprefixpage\" style=\"width:595[.]3pt; height:841[.]9pt;\">" +
    "<div class=\"myprefixdiv\" style=\"left:85[.]05pt; top:36pt; clip:rect[(]0pt,510[.]25pt,74[.]95pt,-85.05pt[)];\">" +
    "<span class=\"myprefixspan myprefixtext001\" style=\"font-size:11pt; left:294[.]73pt; top:0[.]36pt; line-height:12[.]29pt;\">").Success);

outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix/styles.css");

Assert.True(Regex.Match(outDocContents,
    ".myprefixdiv { position:absolute; } " +
    ".myprefixspan { position:absolute; white-space:pre; color:#000000; font-size:12pt; }").Success);
```

### أنظر أيضا

* class [HtmlFixedSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
