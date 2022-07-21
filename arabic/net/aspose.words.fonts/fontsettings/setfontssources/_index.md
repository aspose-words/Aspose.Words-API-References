---
title: SetFontsSources
second_title: Aspose.Words لمراجع .NET API
description: يحدد المصادر حيث يبحث Aspose.Words عن خطوط TrueType عند عرض المستندات أو تضمين الخطوط.
type: docs
weight: 100
url: /ar/net/aspose.words.fonts/fontsettings/setfontssources/
---
## SetFontsSources(FontSourceBase[]) {#setfontssources}

يحدد المصادر حيث يبحث Aspose.Words عن خطوط TrueType عند عرض المستندات أو تضمين الخطوط.

```csharp
public void SetFontsSources(FontSourceBase[] sources)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| sources | FontSourceBase[] | مصفوفة من المصادر التي تحتوي على خطوط تروتايب. |

### ملاحظات

بشكل افتراضي ، يبحث Aspose.Words عن الخطوط المثبتة على النظام.

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

### أنظر أيضا

* class [FontSourceBase](../../fontsourcebase)
* class [FontSettings](../../fontsettings)
* مساحة الاسم [Aspose.Words.Fonts](../../fontsettings)
* المجسم [Aspose.Words](../../../)

---

## SetFontsSources(FontSourceBase[], Stream) {#setfontssources_1}

يعيّن المصادر حيث يبحث Aspose.Words عن خطوط TrueType ويقوم بالإضافة إلى ذلك بتحميل ذاكرة التخزين المؤقت للبحث عن الخطوط المحفوظة مسبقًا .

```csharp
public void SetFontsSources(FontSourceBase[] sources, Stream cacheInputStream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| sources | FontSourceBase[] | مصفوفة من المصادر التي تحتوي على خطوط تروتايب. |
| cacheInputStream | Stream | دفق الإدخال مع ذاكرة التخزين المؤقت للبحث عن الخطوط المحفوظة. |

### ملاحظات

سيؤدي تحميل ذاكرة التخزين المؤقت للبحث عن الخطوط المحفوظة مسبقًا إلى تسريع عملية تهيئة ذاكرة التخزين المؤقت للخط. إنه مفيد بشكل خاص عندما يكون الوصول إلى مصادر الخطوط معقدًا (على سبيل المثال ، عند تحميل الخطوط عبر الشبكة).

عند حفظ ذاكرة التخزين المؤقت للبحث عن الخطوط وتحميلها ، يتم تحديد الخطوط الموجودة في المصادر المتوفرة عبر مفتاح التخزين المؤقت.[`SystemFontSource`](../../systemfontsource) و[`FolderFontSource`](../../folderfontsource) مفتاح التخزين المؤقت هو path لملف الخط. إلى عن على[`MemoryFontSource`](../../memoryfontsource) و[`StreamFontSource`](../../streamfontsource) يتم تعريف مفتاح التخزين المؤقت في ملف[`CacheKey`](../../memoryfontsource/cachekey) و[`CacheKey`](../../streamfontsource/cachekey) Properties على التوالي. بالنسبة إلى[`FileFontSource`](../../filefontsource) مفتاح ذاكرة التخزين المؤقت هو إما[`CacheKey`](../../filefontsource/cachekey) أو مسار ملف إذا كان امتداد الملف[`CacheKey`](../../filefontsource/cachekey) هو **لا شيء**.

يوصى بشدة بتوفير مصادر الخط نفسها عند تحميل ذاكرة التخزين المؤقت كما هو الحال في وقت حفظ ذاكرة التخزين المؤقت . قد تؤدي أي تغييرات في مصادر الخطوط (مثل إضافة خطوط جديدة أو نقل ملفات الخط أو تغيير مفتاح ذاكرة التخزين المؤقت) إلى الخط غير الدقيق حل بواسطة Aspose.Words.

### أمثلة

يوضح كيفية تسريع عملية تهيئة ذاكرة التخزين المؤقت للخط.

```csharp
[Test]
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
/// قم بتحميل بيانات الخط عند الحاجة فقط بدلاً من تخزينها في الذاكرة
/// لكامل عمر الكائن "FontSettings".
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

* class [FontSourceBase](../../fontsourcebase)
* class [FontSettings](../../fontsettings)
* مساحة الاسم [Aspose.Words.Fonts](../../fontsettings)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
