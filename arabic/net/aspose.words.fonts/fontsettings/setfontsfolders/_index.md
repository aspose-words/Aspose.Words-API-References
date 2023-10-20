---
title: FontSettings.SetFontsFolders
linktitle: SetFontsFolders
articleTitle: SetFontsFolders
second_title: Aspose.Words لـ .NET
description: FontSettings SetFontsFolders طريقة. يقوم بتعيين المجلدات التي يبحث فيها Aspose.Words عن خطوط TrueType عند عرض المستندات أو تضمين الخطوط في C#.
type: docs
weight: 90
url: /ar/net/aspose.words.fonts/fontsettings/setfontsfolders/
---
## FontSettings.SetFontsFolders method

يقوم بتعيين المجلدات التي يبحث فيها Aspose.Words عن خطوط TrueType عند عرض المستندات أو تضمين الخطوط.

```csharp
public void SetFontsFolders(string[] fontsFolders, bool recursive)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fontsFolders | String[] | مجموعة من المجلدات التي تحتوي على خطوط TrueType. |
| recursive | Boolean | صحيح لفحص المجلدات المحددة بحثًا عن الخطوط بشكل متكرر. |

## ملاحظات

افتراضيًا، يبحث Aspose.Words عن الخطوط المثبتة على النظام.

يؤدي تعيين هذه الخاصية إلى إعادة تعيين ذاكرة التخزين المؤقت لجميع الخطوط التي تم تحميلها مسبقًا.

## أمثلة

يوضح كيفية تعيين أدلة مصدر خطوط متعددة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// لا تحتوي مصادر الخطوط لدينا على الخط الذي استخدمناه للنص في هذا المستند.
// إذا استخدمنا إعدادات الخط هذه أثناء عرض هذا المستند،
// سيقوم Aspose.Words بتطبيق خط احتياطي على النص الذي يحتوي على خط لا يمكن لـ Aspose.Words تحديد موقعه.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// مصادر الخطوط الافتراضية تفتقد الخطين اللذين نستخدمهما في هذا المستند.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// استخدم طريقة "SetFontsFolders" لإنشاء مصدر خط من كل دليل خطوط نمرره كوسيطة أولى.
// قم بتمرير "خطأ" كوسيطة "متكررة" لتضمين الخطوط من جميع ملفات الخطوط الموجودة في الدلائل
// أننا نمرر الوسيطة الأولى، ولكن لا نضمن أي خطوط من أي من المجلدات الفرعية للمجلدات.
// قم بتمرير "صحيح" كوسيطة "متكررة" لتضمين جميع ملفات الخطوط في الأدلة التي نمررها
// في الوسيطة الأولى، وكذلك جميع الخطوط الموجودة في أدلةها الفرعية.
FontSettings.DefaultInstance.SetFontsFolders(new[] {FontsDir + "/Amethysta", FontsDir + "/Junction"},
    recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(2, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.AreEqual(1, newFontSources[0].GetAvailableFonts().Count);
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// لا يحتوي المجلد "Junction" نفسه على ملفات خطوط، ولكنه يحتوي على مجلدات فرعية تقوم بذلك.
if (recursive)
{
    Assert.AreEqual(6, newFontSources[1].GetAvailableFonts().Count);
    Assert.True(newFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));
}
else
{
    Assert.AreEqual(0, newFontSources[1].GetAvailableFonts().Count);
}

doc.Save(ArtifactsDir + "FontSettings.SetFontsFolders.pdf");

// استعادة مصادر الخط الأصلي.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### أنظر أيضا

* class [FontSettings](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
