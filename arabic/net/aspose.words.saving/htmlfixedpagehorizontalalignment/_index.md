---
title: Enum HtmlFixedPageHorizontalAlignment
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.HtmlFixedPageHorizontalAlignment تعداد. يحدد المحاذاة الأفقية للصفحات في مستند HTML الناتج.
type: docs
weight: 4810
url: /ar/net/aspose.words.saving/htmlfixedpagehorizontalalignment/
---
## HtmlFixedPageHorizontalAlignment enumeration

يحدد المحاذاة الأفقية للصفحات في مستند HTML الناتج.

```csharp
public enum HtmlFixedPageHorizontalAlignment
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Left | `0` | محاذاة الصفحات إلى اليسار . |
| Center | `1` | صفحات المركز. هذه هي القيمة الافتراضية. |
| Right | `2` | محاذاة الصفحات إلى اليمين . |

### أمثلة

يوضح كيفية تعيين المحاذاة الأفقية للصفحات عند حفظ مستند بتنسيق HTML.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    PageHorizontalAlignment = pageHorizontalAlignment
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HorizontalAlignment.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.HorizontalAlignment/styles.css");

switch (pageHorizontalAlignment)
{
    case HtmlFixedPageHorizontalAlignment.Center:
        Assert.True(Regex.Match(outDocContents,
            "[.]awpage { position:relative; border:solid 1pt black; margin:10pt auto 10pt auto; overflow:hidden; }").Success);
        break;
    case HtmlFixedPageHorizontalAlignment.Left:
        Assert.True(Regex.Match(outDocContents, 
            "[.]awpage { position:relative; border:solid 1pt black; margin:10pt auto 10pt 10pt; overflow:hidden; }").Success);
        break;
    case HtmlFixedPageHorizontalAlignment.Right:
        Assert.True(Regex.Match(outDocContents, 
            "[.]awpage { position:relative; border:solid 1pt black; margin:10pt 10pt 10pt auto; overflow:hidden; }").Success);
        break;
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


