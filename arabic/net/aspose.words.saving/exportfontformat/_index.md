---
title: ExportFontFormat Enum
linktitle: ExportFontFormat
articleTitle: ExportFontFormat
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Saving.ExportFontFormat تعداد. يشير إلى التنسيق المستخدم لتصدير الخطوط أثناء العرض إلى تنسيق HTML ثابت في C#.
type: docs
weight: 4990
url: /ar/net/aspose.words.saving/exportfontformat/
---
## ExportFontFormat enumeration

يشير إلى التنسيق المستخدم لتصدير الخطوط أثناء العرض إلى تنسيق HTML ثابت.

```csharp
public enum ExportFontFormat
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Woff | `0` | WOFF (تنسيق الخط المفتوح على الويب). |
| Ttf | `1` | TTF (تنسيق خط TrueType). |

## أمثلة

يوضح كيفية استخدام الخطوط فقط من الجهاز المستهدف عند حفظ مستند بتنسيق HTML.

```csharp
Document doc = new Document(MyDir + "Bullet points with alternative font.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedCss = true,
    UseTargetMachineFonts = useTargetMachineFonts,
    FontFormat = ExportFontFormat.Ttf,
    ExportEmbeddedFonts = false,
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html");

if (useTargetMachineFonts)
    Assert.False(Regex.Match(outDocContents, "@font-face").Success);
else
    Assert.True(Regex.Match(outDocContents,
        "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], " +
        "url[(]'HtmlFixedSaveOptions.UsingMachineFonts/font001.ttf'[)] format[(]'truetype'[)]; }").Success);
```

### أنظر أيضا

* property [FontFormat](../htmlfixedsaveoptions/fontformat/)
* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
