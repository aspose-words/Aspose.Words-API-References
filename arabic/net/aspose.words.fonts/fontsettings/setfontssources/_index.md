---
title: FontSettings.SetFontsSources
second_title: Aspose.Words لمراجع .NET API
description: FontSettings طريقة. يعين المصادر حيث يبحث Aspose.Words عن خطوط TrueType عند عرض المستندات أو تضمين الخطوط.
type: docs
weight: 100
url: /ar/net/aspose.words.fonts/fontsettings/setfontssources/
---
## SetFontsSources(FontSourceBase[]) {#setfontssources}

يعين المصادر حيث يبحث Aspose.Words عن خطوط TrueType عند عرض المستندات أو تضمين الخطوط.

```csharp
public void SetFontsSources(FontSourceBase[] sources)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| sources | FontSourceBase[] | مجموعة من المصادر التي تحتوي على خطوط TrueType. |

### ملاحظات

افتراضيًا، يبحث Aspose.Words عن الخطوط المثبتة على النظام.

يؤدي تعيين هذه الخاصية إلى إعادة تعيين ذاكرة التخزين المؤقت لجميع الخطوط التي تم تحميلها مسبقًا.

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
* مساحة الاسم [Aspose.Words.Fonts](../../fontsettings/)
* المجسم [Aspose.Words](../../../)

---

## SetFontsSources(FontSourceBase[], Stream) {#setfontssources_1}

يعين المصادر حيث يبحث Aspose.Words عن خطوط TrueType ويقوم بالإضافة إلى ذلك بتحميل ذاكرة التخزين المؤقت للبحث عن الخطوط المحفوظة مسبقًا.

```csharp
public void SetFontsSources(FontSourceBase[] sources, Stream cacheInputStream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| sources | FontSourceBase[] | مجموعة من المصادر التي تحتوي على خطوط TrueType. |
| cacheInputStream | Stream | دفق الإدخال مع ذاكرة التخزين المؤقت للبحث عن الخطوط المحفوظة. |

### ملاحظات

سيؤدي تحميل ذاكرة التخزين المؤقت للبحث عن الخطوط المحفوظة مسبقًا إلى تسريع عملية تهيئة ذاكرة التخزين المؤقت للخط. إنه مفيد بشكل خاص عندما يكون الوصول إلى مصادر الخطوط معقدًا (على سبيل المثال، عندما يتم تحميل الخطوط عبر الشبكة).

عند حفظ وتحميل ذاكرة التخزين المؤقت للبحث عن الخطوط، يتم تحديد الخطوط الموجودة في المصادر المتوفرة عبر مفتاح ذاكرة التخزين المؤقت. بالنسبة للخطوط الموجودة في[`SystemFontSource`](../../systemfontsource/) و[`FolderFontSource`](../../folderfontsource/) مفتاح ذاكرة التخزين المؤقت هو path لملف الخط. ل[`MemoryFontSource`](../../memoryfontsource/) و[`StreamFontSource`](../../streamfontsource/) يتم تعريف مفتاح ذاكرة التخزين المؤقت في ملف[`CacheKey`](../../memoryfontsource/cachekey/) و[`CacheKey`](../../streamfontsource/cachekey/) property على التوالي. ل[`FileFontSource`](../../filefontsource/) مفتاح ذاكرة التخزين المؤقت هو إما[`CacheKey`](../../filefontsource/cachekey/) أو مسار الملف إذا كان[`CacheKey`](../../filefontsource/cachekey/) يكون`باطل`.

يوصى بشدة بتوفير نفس مصادر الخطوط عند تحميل ذاكرة التخزين المؤقت كما كانت في وقت حفظ ذاكرة التخزين المؤقت. أي تغييرات في مصادر الخطوط (مثل إضافة خطوط جديدة أو نقل ملفات الخطوط أو تغيير مفتاح ذاكرة التخزين المؤقت) قد تؤدي إلى خط غير دقيق حل بواسطة Aspose.Words.

### أمثلة

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
* مساحة الاسم [Aspose.Words.Fonts](../../fontsettings/)
* المجسم [Aspose.Words](../../../)


