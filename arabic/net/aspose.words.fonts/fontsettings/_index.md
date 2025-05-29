---
title: FontSettings Class
linktitle: FontSettings
articleTitle: FontSettings
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fonts.FontSettings لتخصيص إعدادات خط المستند بسهولة لتحسين قابلية القراءة والعرض الاحترافي.
type: docs
weight: 3400
url: /ar/net/aspose.words.fonts/fontsettings/
---
## FontSettings class

يحدد إعدادات الخط للمستند.

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
| [FallbackSettings](../../aspose.words.fonts/fontsettings/fallbacksettings/) { get; } | الإعدادات المتعلقة بآلية الرجوع إلى الخط. |
| [SubstitutionSettings](../../aspose.words.fonts/fontsettings/substitutionsettings/) { get; } | الإعدادات المتعلقة بآلية استبدال الخط. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFontsSources](../../aspose.words.fonts/fontsettings/getfontssources/)() | يحصل على نسخة من المصفوفة التي تحتوي على قائمة المصادر التي يبحث فيها Aspose.Words عن خطوط TrueType. |
| [ResetFontSources](../../aspose.words.fonts/fontsettings/resetfontsources/)() | إعادة تعيين مصادر الخطوط إلى الإعدادات الافتراضية للنظام. |
| [SaveSearchCache](../../aspose.words.fonts/fontsettings/savesearchcache/)(*Stream*) | يحفظ ذاكرة التخزين المؤقت لبحث الخط في التدفق. |
| [SetFontsFolder](../../aspose.words.fonts/fontsettings/setfontsfolder/)(*string, bool*) | يحدد المجلد الذي يبحث فيه Aspose.Words عن خطوط TrueType عند عرض المستندات أو تضمين الخطوط. هذا اختصار لـ[`SetFontsFolders`](./setfontsfolders/) لتعيين دليل خط واحد فقط. |
| [SetFontsFolders](../../aspose.words.fonts/fontsettings/setfontsfolders/)(*string[], bool*) | يحدد المجلدات التي يبحث فيها Aspose.Words عن خطوط TrueType عند عرض المستندات أو تضمين الخطوط. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources/#setfontssources)(*FontSourceBase[]*) | يحدد المصادر التي يبحث فيها Aspose.Words عن خطوط TrueType عند عرض المستندات أو تضمين الخطوط. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources/#setfontssources_1)(*FontSourceBase[], Stream*) | يحدد المصادر التي يبحث فيها Aspose.Words عن خطوط TrueType ويقوم أيضًا بتحميل ذاكرة التخزين المؤقت للبحث عن الخطوط المحفوظة مسبقًا . |

## ملاحظات

يستخدم Aspose.Words إعدادات الخطوط لتحليل الخطوط في المستند. يتم تحليل الخطوط غالبًا عند إنشاء layout للمستند أو عرضه بتنسيقات صفحات ثابتة. ولكن عند تحميل بعض التنسيقات، قد يتطلب Aspose.Words أيضًا تحليل الخطوط. على سبيل المثال، عند تحميل مستندات HTML عند x000d_، قد يقوم Aspose.Words بتحليل الخطوط لإجراء عملية الرجوع إلى الوضع الطبيعي. لذلك، يُنصح بضبط إعدادات الخطوط في in .[`LoadOptions`](../../aspose.words.loading/loadoptions/) عند تحميل المستند، أو على الأقل قبل إنشاء التخطيط أو عرض المستند بتنسيق الصفحة الثابتة.

افتراضيًا، تستخدم جميع المستندات نموذجًا واحدًا لإعدادات الخط الثابت. يمكن الوصول إليه بواسطة [`DefaultInstance`](./defaultinstance/) ملكية.

تغيير إعدادات الخط آمن في أي وقت ومن أي موضوع. ولكن يُنصح بعدم تغيير إعدادات الخط أثناء معالجة بعض المستندات التي تستخدم هذه الإعدادات. قد يؤدي هذا إلى اختلاف دقة الخط نفسه في أجزاء مختلفة من المستند.

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

* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../)
