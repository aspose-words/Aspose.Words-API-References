---
title: FontSettings.GetFontsSources
linktitle: GetFontsSources
articleTitle: GetFontsSources
second_title: Aspose.Words لـ .NET
description: FontSettings GetFontsSources طريقة. الحصول على نسخة من المصفوفة التي تحتوي على قائمة المصادر حيث يبحث Aspose.Words عن خطوط TrueType في C#.
type: docs
weight: 50
url: /ar/net/aspose.words.fonts/fontsettings/getfontssources/
---
## FontSettings.GetFontsSources method

الحصول على نسخة من المصفوفة التي تحتوي على قائمة المصادر حيث يبحث Aspose.Words عن خطوط TrueType.

```csharp
public FontSourceBase[] GetFontsSources()
```

### قيمة الإرجاع

نسخة من مصادر الخطوط الحالية.

## ملاحظات

القيمة التي تم إرجاعها هي نسخة من البيانات التي يستخدمها Aspose.Words. إذا قمت بتغيير الإدخالات في المصفوفة التي تم إرجاعها، فلن يكون لذلك أي تأثير على عرض المستند. لتحديد مصادر الخطوط الجديدة استخدم[`SetFontsSources`](../setfontssources/) طريقة.

## أمثلة

يوضح كيفية إضافة مصدر خط إلى مصادر الخطوط الموجودة لدينا.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);

Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// مصدر الخط الافتراضي يفتقد اثنين من الخطوط التي نستخدمها في وثيقتنا.
// عندما نحفظ هذا المستند، سيقوم Aspose.Words بتطبيق الخطوط الاحتياطية على كل النص المنسق بخطوط لا يمكن الوصول إليها.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// قم بإنشاء مصدر خط من مجلد يحتوي على الخطوط.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// قم بتطبيق مجموعة جديدة من مصادر الخطوط التي تحتوي على مصادر الخطوط الأصلية، بالإضافة إلى الخطوط المخصصة لدينا.
FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
FontSettings.DefaultInstance.SetFontsSources(updatedFontSources);

// تحقق من أن Aspose.Words لديه حق الوصول إلى جميع الخطوط المطلوبة قبل تحويل المستند إلى PDF.
updatedFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.True(updatedFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

doc.Save(ArtifactsDir + "FontSettings.AddFontSource.pdf");

// استعادة مصادر الخط الأصلي.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### أنظر أيضا

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
