---
title: FontSettings.SetFontsSources
linktitle: SetFontsSources
articleTitle: SetFontsSources
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل طريقة SetFontsSources في Aspose.Words على تحسين عرض المستندات من خلال تحديد مصادر الخطوط TrueType للحصول على أفضل النتائج.
type: docs
weight: 100
url: /ar/net/aspose.words.fonts/fontsettings/setfontssources/
---
## SetFontsSources(*FontSourceBase[]*) {#setfontssources}

يحدد المصادر التي يبحث فيها Aspose.Words عن خطوط TrueType عند عرض المستندات أو تضمين الخطوط.

```csharp
public void SetFontsSources(FontSourceBase[] sources)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| sources | FontSourceBase[] | مجموعة من المصادر التي تحتوي على خطوط TrueType. |

## ملاحظات

بشكل افتراضي، يبحث Aspose.Words عن الخطوط المثبتة على النظام.

يؤدي تعيين هذه الخاصية إلى إعادة تعيين ذاكرة التخزين المؤقت لجميع الخطوط التي تم تحميلها مسبقًا.

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

---

## SetFontsSources(*FontSourceBase[], Stream*) {#setfontssources_1}

يحدد المصادر التي يبحث فيها Aspose.Words عن خطوط TrueType ويقوم أيضًا بتحميل ذاكرة التخزين المؤقت للبحث عن الخطوط المحفوظة مسبقًا .

```csharp
public void SetFontsSources(FontSourceBase[] sources, Stream cacheInputStream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| sources | FontSourceBase[] | مجموعة من المصادر التي تحتوي على خطوط TrueType. |
| cacheInputStream | Stream | تدفق الإدخال مع ذاكرة التخزين المؤقت للبحث عن الخطوط المحفوظة. |

## ملاحظات

سيؤدي تحميل ذاكرة التخزين المؤقت لبحث الخطوط المحفوظة مسبقًا إلى تسريع عملية تهيئة ذاكرة التخزين المؤقت للخطوط. وهو مفيد بشكل خاص عندما يكون الوصول إلى مصادر الخطوط معقدًا (مثلاً عند تحميل الخطوط عبر الشبكة).

عند حفظ ذاكرة التخزين المؤقت لبحث الخطوط وتحميلها، يتم التعرف على الخطوط الموجودة في المصادر المقدمة عبر مفتاح ذاكرة التخزين المؤقت. بالنسبة للخطوط الموجودة في[`SystemFontSource`](../../systemfontsource/) و[`FolderFontSource`](../../folderfontsource/) مفتاح التخزين المؤقت هو المسار لملف الخط.[`MemoryFontSource`](../../memoryfontsource/) و[`StreamFontSource`](../../streamfontsource/)مفتاح التخزين المؤقت هو defined في[`CacheKey`](../../memoryfontsource/cachekey/) و[`CacheKey`](../../streamfontsource/cachekey/) properties على التوالي. بالنسبة لـ[`FileFontSource`](../../filefontsource/) مفتاح التخزين المؤقت هو إما[`CacheKey`](../../filefontsource/cachekey/) الخاصية أو مسار الملف إذا كان[`CacheKey`](../../filefontsource/cachekey/) يكون`باطل`.

يوصى بشدة بتوفير نفس مصادر الخطوط عند تحميل ذاكرة التخزين المؤقت كما في وقت حفظ ذاكرة التخزين المؤقت. قد تؤدي أي تغييرات في مصادر الخطوط (مثل إضافة خطوط جديدة أو نقل ملفات الخطوط أو تغيير مفتاح ذاكرة التخزين المؤقت) إلى حل الخط غير الدقيق بواسطة Aspose.Words.

## أمثلة

يوضح كيفية تسريع عملية تهيئة ذاكرة التخزين المؤقت للخط.

```csharp
public void LoadFontSearchCache()
{
    const string cacheKey1 = "Arvo";
    const string cacheKey2 = "Arvo-Bold";
    FontSettings parsedFonts = new FontSettings();
    FontSettings loadedCache = new FontSettings();

    parsedFonts.SetFontsSources(new FontSourceBase[]
    {
        new FileFontSource(FontsDir + "Arvo-Regular.ttf", 0, cacheKey1),
        new FileFontSource(FontsDir + "Arvo-Bold.ttf", 0, cacheKey2)
    });

    using (MemoryStream cacheStream = new MemoryStream())
    {
        parsedFonts.SaveSearchCache(cacheStream);
        loadedCache.SetFontsSources(new FontSourceBase[]
        {
            new SearchCacheStream(cacheKey1),
            new MemoryFontSource(File.ReadAllBytes(FontsDir + "Arvo-Bold.ttf"), 0, cacheKey2)
        }, cacheStream);
    }

    Assert.AreEqual(parsedFonts.GetFontsSources().Length, loadedCache.GetFontsSources().Length);
}

/// <summary>
/// قم بتحميل بيانات الخط فقط عند الحاجة إليها بدلاً من تخزينها في الذاكرة
/// طوال عمر كائن "FontSettings".
/// </summary>
private class SearchCacheStream : StreamFontSource
{
    public SearchCacheStream(string cacheKey):base(0, cacheKey)
    {
    }

    public override Stream OpenFontDataStream()
    {
        return File.OpenRead(FontsDir + "Arvo-Regular.ttf");
    }
}
```

### أنظر أيضا

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
