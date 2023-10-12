---
title: FontSettings.SetFontsFolder
second_title: Aspose.Words لمراجع .NET API
description: FontSettings طريقة. يعين المجلد الذي يبحث فيه Aspose.Words عن خطوط TrueType عند عرض المستندات أو تضمين الخطوط. هذا اختصار لـSetFontsFolders لتعيين دليل خط واحد فقط.
type: docs
weight: 80
url: /ar/net/aspose.words.fonts/fontsettings/setfontsfolder/
---
## FontSettings.SetFontsFolder method

يعين المجلد الذي يبحث فيه Aspose.Words عن خطوط TrueType عند عرض المستندات أو تضمين الخطوط. هذا اختصار لـ[`SetFontsFolders`](../setfontsfolders/) لتعيين دليل خط واحد فقط.

```csharp
public void SetFontsFolder(string fontFolder, bool recursive)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fontFolder | String | المجلد الذي يحتوي على خطوط تروتايب. |
| recursive | Boolean | صحيح لفحص المجلدات المحددة بحثًا عن الخطوط بشكل متكرر. |

### أمثلة

يوضح كيفية تعيين دليل مصدر الخط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arvo";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// لا تحتوي مصادر الخطوط لدينا على الخط الذي استخدمناه للنص في هذا المستند.
// إذا استخدمنا إعدادات الخط هذه أثناء عرض هذا المستند،
// سيقوم Aspose.Words بتطبيق خط احتياطي على النص الذي يحتوي على خط لا يمكن لـ Aspose.Words تحديد موقعه.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// مصادر الخطوط الافتراضية تفتقد الخطين اللذين نستخدمهما في هذا المستند.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// استخدم طريقة "SetFontsFolder" لتعيين دليل سيكون بمثابة مصدر خط جديد.
// قم بتمرير "خطأ" كوسيطة "متكررة" لتضمين الخطوط من جميع ملفات الخطوط الموجودة في الدليل
// أننا نقوم بتمرير الوسيطة الأولى، ولكن لا نقوم بتضمين أي خطوط في أي من المجلدات الفرعية لهذا الدليل.
// قم بتمرير "صحيح" كوسيطة "متكررة" لتضمين جميع ملفات الخطوط في الدليل الذي نمرره
// في الوسيطة الأولى، وكذلك جميع الخطوط الموجودة في أدلةها الفرعية.
FontSettings.DefaultInstance.SetFontsFolder(FontsDir, recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// الخط "Amethysta" موجود في مجلد فرعي لدليل الخطوط.
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

// استعادة مصادر الخط الأصلي.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### أنظر أيضا

* class [FontSettings](../)
* مساحة الاسم [Aspose.Words.Fonts](../../fontsettings/)
* المجسم [Aspose.Words](../../../)


