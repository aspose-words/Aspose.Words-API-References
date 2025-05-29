---
title: HtmlFixedSaveOptions.UseTargetMachineFonts
linktitle: UseTargetMachineFonts
articleTitle: UseTargetMachineFonts
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية UseTargetMachineFonts في HtmlFixedSaveOptions عرض المستندات باستخدام خطوط الآلة المستهدفة. حسّن إدارة خطوطك اليوم!
type: docs
weight: 210
url: /ar/net/aspose.words.saving/htmlfixedsaveoptions/usetargetmachinefonts/
---
## HtmlFixedSaveOptions.UseTargetMachineFonts property

يشير العلم إلى ما إذا كان يجب استخدام الخطوط من الجهاز المستهدف لعرض المستند. إذا تم تعيين هذا العلم على`حقيقي` ،[`FontFormat`](../fontformat/) و[`ExportEmbeddedFonts`](../exportembeddedfonts/) الخصائص ليس لها تأثير، أيضًا[`ResourceSavingCallback`](../resourcesavingcallback/) لا يتم تشغيله للخطوط. الافتراضي هو`خطأ شنيع` .

```csharp
public bool UseTargetMachineFonts { get; set; }
```

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

* class [HtmlFixedSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
