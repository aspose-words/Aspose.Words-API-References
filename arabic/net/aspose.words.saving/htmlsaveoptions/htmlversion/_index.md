---
title: HtmlSaveOptions.HtmlVersion
linktitle: HtmlVersion
articleTitle: HtmlVersion
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية HtmlSaveOptions HtmlVersion لاختيار معيار HTML بسهولة عند حفظ المستندات بتنسيق HTML أو MHTML. حسّن إنتاجيتك بسهولة!
type: docs
weight: 330
url: /ar/net/aspose.words.saving/htmlsaveoptions/htmlversion/
---
## HtmlSaveOptions.HtmlVersion property

يحدد إصدار معيار HTML الذي يجب استخدامه عند حفظ المستند بتنسيق HTML أو MHTML. القيمة الافتراضية هيXhtml .

```csharp
public HtmlVersion HtmlVersion { get; set; }
```

## أمثلة

يوضح كيفية عرض عنوان DOCTYPE عند تحويل المستندات إلى معيار الانتقال Xhtml 1.0.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    HtmlVersion = HtmlVersion.Xhtml,
    ExportXhtmlTransitional = showDoctypeDeclaration,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html", options);

// ستحتوي مستندنا فقط على عنوان إعلان DOCTYPE إذا قمنا بتعيين علامة "ExportXhtmlTransitional" إلى "true".
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html");
string newLine = Environment.NewLine;

if (showDoctypeDeclaration)
    Assert.True(outDocContents.Contains(
        $"<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>{newLine}" +
        $"<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 انتقالي//EN\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">{سطر جديد}" +
        "<html xmlns=\"http://www.w3.org/1999/xhtml\">"));
else
    Assert.True(outDocContents.Contains("<html>"));
```

يوضح كيفية حفظ مستند إلى إصدار محدد من HTML.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    HtmlVersion = htmlVersion,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.HtmlVersions.html", options);

// ستحتوي مستندات HTML الخاصة بنا على اختلافات طفيفة لتكون متوافقة مع إصدارات HTML المختلفة.
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.HtmlVersions.html");

switch (htmlVersion)
{
    case HtmlVersion.Html5:
        Assert.True(outDocContents.Contains("<a id=\"_Toc76372689\"></a>"));
        Assert.True(outDocContents.Contains("<a id=\"_Toc76372689\"></a>"));
        Assert.True(outDocContents.Contains("<table style=\"padding:0pt; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
        break;
    case HtmlVersion.Xhtml:
        Assert.True(outDocContents.Contains("<a name=\"_Toc76372689\"></a>"));
        Assert.True(outDocContents.Contains("<ul type=\"disc\" style=\"margin:0pt; padding-left:0pt\">"));
        Assert.True(outDocContents.Contains("<table cellspacing=\"0\" cellpadding=\"0\" style=\"-aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\""));
        break;
}
```

### أنظر أيضا

* enum [HtmlVersion](../../htmlversion/)
* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
