---
title: FontSettings Class
linktitle: FontSettings
articleTitle: FontSettings
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Fonts.FontSettings فصل. تحديد إعدادات الخط للمستند في C#.
type: docs
weight: 2970
url: /ar/net/aspose.words.fonts/fontsettings/
---
## FontSettings class

تحديد إعدادات الخط للمستند.

لمعرفة المزيد، قم بزيارة[العمل مع الخطوط](https://docs.aspose.com/words/net/working-with-fonts/) مقالة توثيقية.

```csharp
public class FontSettings
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FontSettings](fontsettings/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| static [DefaultInstance](../../aspose.words.fonts/fontsettings/defaultinstance/) { get; } | إعدادات الخط الافتراضية الثابتة. |
| [FallbackSettings](../../aspose.words.fonts/fontsettings/fallbacksettings/) { get; } | الإعدادات المتعلقة بآلية الرجوع للخط. |
| [SubstitutionSettings](../../aspose.words.fonts/fontsettings/substitutionsettings/) { get; } | الإعدادات المتعلقة بآلية استبدال الخطوط. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFontsSources](../../aspose.words.fonts/fontsettings/getfontssources/)() | الحصول على نسخة من المصفوفة التي تحتوي على قائمة المصادر حيث يبحث Aspose.Words عن خطوط TrueType. |
| [ResetFontSources](../../aspose.words.fonts/fontsettings/resetfontsources/)() | إعادة ضبط مصادر الخطوط إلى الوضع الافتراضي للنظام. |
| [SaveSearchCache](../../aspose.words.fonts/fontsettings/savesearchcache/)(*Stream*) | يحفظ ذاكرة التخزين المؤقت للبحث عن الخطوط في الدفق. |
| [SetFontsFolder](../../aspose.words.fonts/fontsettings/setfontsfolder/)(*string, bool*) | يعين المجلد الذي يبحث فيه Aspose.Words عن خطوط TrueType عند عرض المستندات أو تضمين الخطوط. هذا اختصار لـ[`SetFontsFolders`](./setfontsfolders/) لتعيين دليل خط واحد فقط. |
| [SetFontsFolders](../../aspose.words.fonts/fontsettings/setfontsfolders/)(*string[], bool*) | يقوم بتعيين المجلدات التي يبحث فيها Aspose.Words عن خطوط TrueType عند عرض المستندات أو تضمين الخطوط. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources/#setfontssources)(*FontSourceBase[]*) | يعين المصادر حيث يبحث Aspose.Words عن خطوط TrueType عند عرض المستندات أو تضمين الخطوط. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources/#setfontssources_1)(*FontSourceBase[], Stream*) | يعين المصادر حيث يبحث Aspose.Words عن خطوط TrueType ويقوم بالإضافة إلى ذلك بتحميل ذاكرة التخزين المؤقت للبحث عن الخطوط المحفوظة مسبقًا. |

## ملاحظات

يستخدم Aspose.Words إعدادات الخط لتحليل الخطوط الموجودة في المستند. يتم حل الخطوط في الغالب عند إنشاء تخطيط مستند أو عرضه على تنسيقات صفحات ثابتة. ولكن عند تحميل بعض التنسيقات، قد يتطلب Aspose.Words أيضًا حل الخطوط. على سبيل المثال، عند تحميل مستندات HTML قد يقوم Aspose.Words بتحليل الخطوط لتنفيذ خط احتياطي. لذا يوصى بضبط إعدادات الخط in [`LoadOptions`](../../aspose.words.loading/loadoptions/) عند تحميل المستند. أو على الأقل قبل إنشاء التخطيط أو عرض المستند إلى تنسيق الصفحة الثابتة.

افتراضيًا، تستخدم جميع المستندات مثيلًا واحدًا لإعدادات الخط الثابت. يمكن الوصول إليه بواسطة [`DefaultInstance`](./defaultinstance/) ملكية.

يعد تغيير إعدادات الخط آمنًا في أي وقت ومن أي موضوع. ولكن يوصى بعدم تغيير إعدادات الخط أثناء معالجة بعض المستندات التي تستخدم هذه الإعدادات. يمكن أن يؤدي هذا إلى حقيقة أنه سيتم حل نفس الخط بشكل مختلف في أجزاء مختلفة من المستند.

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

* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../)
