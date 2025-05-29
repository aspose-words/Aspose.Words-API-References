---
title: FontSettings.GetFontsSources
linktitle: GetFontsSources
articleTitle: GetFontsSources
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة FontSettings GetFontsSources للوصول بسهولة إلى مجموعة مصادر خطوط TrueType في Aspose.Words. حسّن إدارة خطوطك اليوم!
type: docs
weight: 50
url: /ar/net/aspose.words.fonts/fontsettings/getfontssources/
---
## FontSettings.GetFontsSources method

يحصل على نسخة من المصفوفة التي تحتوي على قائمة المصادر التي يبحث فيها Aspose.Words عن خطوط TrueType.

```csharp
public FontSourceBase[] GetFontsSources()
```

### قيمة الإرجاع

نسخة من مصادر الخط الحالية.

## ملاحظات

القيمة المُعادة هي نسخة من البيانات التي يستخدمها Aspose.Words. إذا غيّرت entrys في المصفوفة المُعادة، فلن يؤثر ذلك على عرض المستند. لتحديد مصادر خطوط جديدة، استخدم[`SetFontsSources`](../setfontssources/) طريقة.

## أمثلة

يوضح كيفية إضافة مصدر الخط إلى مصادر الخطوط الموجودة لدينا.

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

//يفتقد مصدر الخط الافتراضي اثنين من الخطوط التي نستخدمها في مستندنا.
// عندما نحفظ هذا المستند، سيقوم Aspose.Words بتطبيق الخطوط البديلة على كل النص المنسق بخطوط غير قابلة للوصول.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// قم بإنشاء مصدر الخط من مجلد يحتوي على الخطوط.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// قم بتطبيق مجموعة جديدة من مصادر الخطوط التي تحتوي على مصادر الخطوط الأصلية، بالإضافة إلى الخطوط المخصصة لدينا.
FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
FontSettings.DefaultInstance.SetFontsSources(updatedFontSources);

// تأكد من أن Aspose.Words لديه إمكانية الوصول إلى جميع الخطوط المطلوبة قبل تقديم المستند إلى PDF.
updatedFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.True(updatedFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

doc.Save(ArtifactsDir + "FontSettings.AddFontSource.pdf");

//استعادة مصادر الخط الأصلية.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### أنظر أيضا

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
