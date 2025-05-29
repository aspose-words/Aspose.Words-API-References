---
title: FontSettings.SetFontsFolders
linktitle: SetFontsFolders
articleTitle: SetFontsFolders
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية استخدام طريقة SetFontsFolders في Aspose.Words لتخصيص مواقع خطوط TrueType للحصول على أفضل عرض وتضمين للمستندات.
type: docs
weight: 90
url: /ar/net/aspose.words.fonts/fontsettings/setfontsfolders/
---
## FontSettings.SetFontsFolders method

يحدد المجلدات التي يبحث فيها Aspose.Words عن خطوط TrueType عند عرض المستندات أو تضمين الخطوط.

```csharp
public void SetFontsFolders(string[] fontsFolders, bool recursive)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fontsFolders | String[] | مجموعة من المجلدات التي تحتوي على خطوط TrueType. |
| recursive | Boolean | صحيح لمسح المجلدات المحددة للخطوط بشكل متكرر. |

## ملاحظات

بشكل افتراضي، يبحث Aspose.Words عن الخطوط المثبتة على النظام.

يؤدي تعيين هذه الخاصية إلى إعادة تعيين ذاكرة التخزين المؤقت لجميع الخطوط التي تم تحميلها مسبقًا.

## أمثلة

يوضح كيفية تعيين أدلة مصدر الخطوط المتعددة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

//لا تحتوي مصادر الخطوط لدينا على الخط الذي استخدمناه للنص في هذه الوثيقة.
// إذا استخدمنا إعدادات الخط هذه أثناء عرض هذا المستند،
// سيقوم Aspose.Words بتطبيق خط احتياطي على النص الذي يحتوي على خط لا يستطيع Aspose.Words تحديد موقعه.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// مصادر الخطوط الافتراضية تفتقر إلى الخطين اللذين نستخدمهما في هذه الوثيقة.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// استخدم طريقة "SetFontsFolders" لإنشاء مصدر خط من كل دليل خط نمرره كحجة أولى.
// قم بتمرير "false" كحجة "متكررة" لتضمين الخطوط من جميع ملفات الخطوط الموجودة في الدلائل
// أننا نمرر الحجة الأولى، ولكن لا نقوم بتضمين أي خطوط من أي من المجلدات الفرعية للمجلدات.
// قم بتمرير "true" كحجة "متكررة" لتضمين جميع ملفات الخطوط في الدلائل التي نمررها
// في الحجة الأولى، وكذلك جميع الخطوط الموجودة في الدلائل الفرعية الخاصة بها.
FontSettings.DefaultInstance.SetFontsFolders(new[] {FontsDir + "/Amethysta", FontsDir + "/Junction"},
    recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(2, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.AreEqual(1, newFontSources[0].GetAvailableFonts().Count);
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// لا يحتوي مجلد "Junction" نفسه على ملفات خطوط، ولكنه يحتوي على مجلدات فرعية تحتوي على ملفات خطوط.
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

//استعادة مصادر الخط الأصلية.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### أنظر أيضا

* class [FontSettings](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
