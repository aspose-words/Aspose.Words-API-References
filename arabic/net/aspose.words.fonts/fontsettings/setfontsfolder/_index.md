---
title: FontSettings.SetFontsFolder
linktitle: SetFontsFolder
articleTitle: SetFontsFolder
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية استخدام طريقة SetFontsFolder لتحديد دليل الخط TrueType في Aspose.Words، وتحسين عرض المستندات وتضمين الخطوط.
type: docs
weight: 80
url: /ar/net/aspose.words.fonts/fontsettings/setfontsfolder/
---
## FontSettings.SetFontsFolder method

يحدد المجلد الذي يبحث فيه Aspose.Words عن خطوط TrueType عند عرض المستندات أو تضمين الخطوط. هذا اختصار لـ[`SetFontsFolders`](../setfontsfolders/) لتعيين دليل خط واحد فقط.

```csharp
public void SetFontsFolder(string fontFolder, bool recursive)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fontFolder | String | المجلد الذي يحتوي على خطوط TrueType. |
| recursive | Boolean | صحيح لمسح المجلدات المحددة للخطوط بشكل متكرر. |

## أمثلة

يوضح كيفية تعيين دليل مصدر الخط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arvo";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

//لا تحتوي مصادر الخطوط لدينا على الخط الذي استخدمناه للنص في هذه الوثيقة.
// إذا استخدمنا إعدادات الخط هذه أثناء عرض هذا المستند،
// سيقوم Aspose.Words بتطبيق خط احتياطي على النص الذي يحتوي على خط لا يستطيع Aspose.Words تحديد موقعه.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// مصادر الخطوط الافتراضية تفتقر إلى الخطين اللذين نستخدمهما في هذه الوثيقة.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

//استخدم طريقة "SetFontsFolder" لتعيين الدليل الذي سيعمل كمصدر خط جديد.
// قم بتمرير "false" كحجة "متكررة" لتضمين الخطوط من جميع ملفات الخطوط الموجودة في الدليل
// أننا نمرر الحجة الأولى، ولكن لا نقوم بتضمين أي خطوط في أي من المجلدات الفرعية لهذا الدليل.
// قم بتمرير "true" كحجة "متكررة" لتضمين جميع ملفات الخطوط في الدليل الذي نمرره
// في الحجة الأولى، وكذلك جميع الخطوط الموجودة في الدلائل الفرعية الخاصة بها.
FontSettings.DefaultInstance.SetFontsFolder(FontsDir, recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// الخط "Amethysta" موجود في مجلد فرعي من دليل الخطوط.
if (recursive)
{
    Assert.AreEqual(25, newFontSources[0].GetAvailableFonts().Count);
    Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
}
else
{
    Assert.AreEqual(18, newFontSources[0].GetAvailableFonts().Count);
    Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
}

doc.Save(ArtifactsDir + "FontSettings.SetFontsFolder.pdf");

//استعادة مصادر الخط الأصلية.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### أنظر أيضا

* class [FontSettings](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
