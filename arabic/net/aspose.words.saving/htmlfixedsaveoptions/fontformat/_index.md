---
title: HtmlFixedSaveOptions.FontFormat
second_title: Aspose.Words لمراجع .NET API
description: HtmlFixedSaveOptions ملكية. يحصل على أو مجموعاتExportFontFormat يستخدم لتصدير الخط. القيمة الافتراضية هيWoff .
type: docs
weight: 90
url: /ar/net/aspose.words.saving/htmlfixedsaveoptions/fontformat/
---
## HtmlFixedSaveOptions.FontFormat property

يحصل على أو مجموعات[`ExportFontFormat`](../../exportfontformat/) يستخدم لتصدير الخط. القيمة الافتراضية هيWoff .

```csharp
public ExportFontFormat FontFormat { get; set; }
```

### أمثلة

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

* enum [ExportFontFormat](../../exportfontformat/)
* class [HtmlFixedSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* المجسم [Aspose.Words](../../../)


