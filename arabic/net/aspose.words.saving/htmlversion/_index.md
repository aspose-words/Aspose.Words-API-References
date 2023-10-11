---
title: Enum HtmlVersion
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.HtmlVersion تعداد. يشير إلى إصدار HTML المستخدم عند حفظ المستند فيهHtml و Mhtml التنسيقات.
type: docs
weight: 5120
url: /ar/net/aspose.words.saving/htmlversion/
---
## HtmlVersion enumeration

يشير إلى إصدار HTML المستخدم عند حفظ المستند فيهHtml و Mhtml التنسيقات.

```csharp
public enum HtmlVersion
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Xhtml | `0` | يحفظ المستند بالتوافق مع معيار XHTML 1.0 الانتقالي. |
| Html5 | `1` | يحفظ المستند بالتوافق مع معيار HTML 5. |

### أمثلة

يوضح كيفية عرض عنوان DOCTYPE عند تحويل المستندات إلى المعيار الانتقالي Xhtml 1.0.

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

// ستحتوي وثيقتنا على عنوان إعلان DOCTYPE فقط إذا قمنا بتعيين علامة "ExportXhtmlTransitional" على "true".
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html");

if (showDoctypeDeclaration)
    Assert.True(outDocContents.Contains(
        "<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>\r\n" +
        "<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Transitional//EN\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">\r\n" +
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
        Assert.True(outDocContents.Contains("<table style=\"-aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
        break;
    case HtmlVersion.Xhtml:
        Assert.True(outDocContents.Contains("<a name=\"_Toc76372689\"></a>"));
        Assert.True(outDocContents.Contains("<ul type=\"disc\" style=\"margin:0pt; padding-left:0pt\">"));
        Assert.True(outDocContents.Contains("<table cellspacing=\"0\" cellpadding=\"0\" style=\"-aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\""));
        break;
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


