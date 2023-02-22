---
title: Class FontSettings
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fonts.FontSettings فصل. يحدد إعدادات الخط لمستند .
type: docs
weight: 2790
url: /ar/net/aspose.words.fonts/fontsettings/
---
## FontSettings class

يحدد إعدادات الخط لمستند .

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
| static [DefaultInstance](../../aspose.words.fonts/fontsettings/defaultinstance/) { get; } | إعدادات الخط الافتراضية الثابتة . |
| [FallbackSettings](../../aspose.words.fonts/fontsettings/fallbacksettings/) { get; } | الإعدادات المتعلقة بآلية النسخ الاحتياطي للخط . |
| [SubstitutionSettings](../../aspose.words.fonts/fontsettings/substitutionsettings/) { get; } | الإعدادات المتعلقة بآلية استبدال الخط. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFontsSources](../../aspose.words.fonts/fontsettings/getfontssources/)() | يحصل على نسخة من المصفوفة التي تحتوي على قائمة المصادر حيث يبحث Aspose.Words عن خطوط TrueType . |
| [ResetFontSources](../../aspose.words.fonts/fontsettings/resetfontsources/)() | يعيد تعيين مصادر الخطوط إلى النظام الافتراضي. |
| [SaveSearchCache](../../aspose.words.fonts/fontsettings/savesearchcache/)(Stream) | يحفظ ذاكرة التخزين المؤقت للبحث عن الخط في الدفق. |
| [SetFontsFolder](../../aspose.words.fonts/fontsettings/setfontsfolder/)(string, bool) | يضبط المجلد حيث يبحث Aspose.Words عن خطوط TrueType عند عرض المستندات أو تضمين الخطوط . هذا اختصار لـ[`SetFontsFolders`](./setfontsfolders/) لتعيين دليل خطوط واحد فقط. |
| [SetFontsFolders](../../aspose.words.fonts/fontsettings/setfontsfolders/)(string[], bool) | يضبط المجلدات حيث يبحث Aspose.Words عن خطوط TrueType عند عرض المستندات أو تضمين الخطوط. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources/#setfontssources)(FontSourceBase[]) | يحدد المصادر حيث يبحث Aspose.Words عن خطوط TrueType عند عرض المستندات أو تضمين الخطوط. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources/#setfontssources_1)(FontSourceBase[], Stream) | يعيّن المصادر حيث يبحث Aspose.Words عن خطوط TrueType ويقوم بالإضافة إلى ذلك بتحميل ذاكرة التخزين المؤقت للبحث عن الخطوط المحفوظة مسبقًا . |

### ملاحظات

يستخدم Aspose.Words إعدادات الخطوط لحل الخطوط في الوثيقة. يتم حل الخطوط في الغالب عند إنشاء المستند layout أو تقديمه إلى تنسيقات الصفحات الثابتة. ولكن عند تحميل بعض التنسيقات ، قد يطلب Aspose.Words أيضًا حل الخطوط. على سبيل المثال ، when تحميل مستندات HTML قد يقوم Aspose.Words بحل الخطوط لإجراء احتياطي للخط. لذلك يوصى بضبط إعدادات الخط في [`LoadOptions`](../../aspose.words.loading/loadoptions/) عند تحميل المستند. أو على الأقل قبل إنشاء التخطيط أو تحويل المستند إلى تنسيق الصفحة الثابتة.

بشكل افتراضي ، تستخدم جميع المستندات مثيلًا واحدًا لإعدادات الخط الثابت. يمكن الوصول إليه عن طريق [`DefaultInstance`](./defaultinstance/) منشأه.

تغيير إعدادات الخط آمن في أي وقت من أي موضوع. لكن يوصى بعدم تغيير إعدادات الخط أثناء معالجة بعض المستندات التي تستخدم هذه الإعدادات. يمكن أن يؤدي هذا إلى حقيقة أنه سيتم حل نفس الخط بشكل مختلف في أجزاء مختلفة من المستند.

### أمثلة

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

// يفتقد مصدر الخط الافتراضي إلى اثنين من الخطوط التي نستخدمها في وثيقتنا.
// عندما نحفظ هذا المستند ، ستطبق Aspose.Words الخطوط الاحتياطية على جميع النصوص المنسقة بخطوط لا يمكن الوصول إليها.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// إنشاء مصدر خط من مجلد يحتوي على خطوط.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// قم بتطبيق مجموعة جديدة من مصادر الخطوط التي تحتوي على مصادر الخطوط الأصلية ، بالإضافة إلى الخطوط المخصصة لدينا.
FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
FontSettings.DefaultInstance.SetFontsSources(updatedFontSources);

// تحقق من أن Aspose.Words حق الوصول إلى جميع الخطوط المطلوبة قبل تقديم المستند إلى PDF.
updatedFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.True(updatedFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

doc.Save(ArtifactsDir + "FontSettings.AddFontSource.pdf");

// استعادة مصادر الخط الأصلية.
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
// إذا استخدمنا إعدادات الخط هذه أثناء تقديم هذا المستند ،
// Aspose.Words ستطبق خطًا احتياطيًا على النص الذي يحتوي على خط لا يمكن لـ Aspose.Words تحديد مكانه.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// تفتقد مصادر الخطوط الافتراضية إلى الخطين اللذين نستخدمهما في هذا المستند.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// استخدم طريقة "SetFontsFolder" لتعيين دليل يعمل كمصدر خط جديد.
// تمرير "خطأ" كوسيطة "متكررة" لتضمين الخطوط من كافة ملفات الخطوط الموجودة في الدليل
// أننا نمرر في الوسيطة الأولى ، لكن لا نضمن أي خطوط في أي من المجلدات الفرعية لهذا الدليل.
// تمرير "true" كوسيطة "عودية" لتضمين جميع ملفات الخطوط في الدليل الذي نقوم بتمريره
// في الوسيطة الأولى ، بالإضافة إلى جميع الخطوط الموجودة في مجلداته الفرعية.
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

// استعادة مصادر الخط الأصلية.
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
// إذا استخدمنا إعدادات الخط هذه أثناء تقديم هذا المستند ،
// Aspose.Words ستطبق خطًا احتياطيًا على النص الذي يحتوي على خط لا يمكن لـ Aspose.Words تحديد مكانه.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// تفتقد مصادر الخطوط الافتراضية إلى الخطين اللذين نستخدمهما في هذا المستند.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// استخدم طريقة "SetFontsFolders" لإنشاء مصدر خط من كل دليل خط نقوم بتمريره باعتباره الوسيطة الأولى.
// تمرير "خطأ" كوسيطة "متكررة" لتضمين الخطوط من كافة ملفات الخطوط الموجودة في الدلائل
// أننا نمرر في الوسيطة الأولى ، لكن لا نقوم بتضمين أي خطوط من أي من المجلدات الفرعية للمجلدات.
// قم بتمرير "true" باعتباره الوسيطة "العودية" لتضمين جميع ملفات الخطوط في الدلائل التي نقوم بتمريرها
// في الوسيطة الأولى ، بالإضافة إلى جميع الخطوط في الدلائل الفرعية الخاصة بهم.
FontSettings.DefaultInstance.SetFontsFolders(new[] {FontsDir + "/Amethysta", FontsDir + "/Junction"},
    recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(2, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.AreEqual(1, newFontSources[0].GetAvailableFonts().Count);
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// لا يحتوي مجلد "Junction" نفسه على ملفات خطوط ، ولكنه يحتوي على مجلدات فرعية تعمل.
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

// استعادة مصادر الخط الأصلية.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../)


