---
title: StreamFontSource.CacheKey
linktitle: CacheKey
articleTitle: CacheKey
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية StreamFontSource CacheKey، وقم بتحسين إدارة الخطوط لديك باستخدام التخزين المؤقت الفعال للحصول على أوقات تحميل أسرع وأداء محسّن.
type: docs
weight: 10
url: /ar/net/aspose.words.fonts/streamfontsource/cachekey/
---
## StreamFontSource.CacheKey property

مفتاح هذا المصدر في ذاكرة التخزين المؤقت.

```csharp
public string CacheKey { get; }
```

## ملاحظات

يستخدم هذا المفتاح لتحديد عنصر ذاكرة التخزين المؤقت عند حفظ/تحميل ذاكرة التخزين المؤقت لبحث الخط باستخدام [`SaveSearchCache`](../../fontsettings/savesearchcache/) و[`SetFontsSources`](../../fontsettings/setfontssources/) الأساليب.

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

* class [StreamFontSource](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
