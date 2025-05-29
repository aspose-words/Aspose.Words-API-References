---
title: FontSettings.SaveSearchCache
linktitle: SaveSearchCache
articleTitle: SaveSearchCache
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تقوم طريقة SaveSearchCache الخاصة بـ FontSettings بحفظ ذاكرة التخزين المؤقت لبحث الخطوط الخاصة بك بكفاءة في مجرى، مما يعزز الأداء وتجربة المستخدم.
type: docs
weight: 70
url: /ar/net/aspose.words.fonts/fontsettings/savesearchcache/
---
## FontSettings.SaveSearchCache method

يحفظ ذاكرة التخزين المؤقت لبحث الخط في التدفق.

```csharp
public void SaveSearchCache(Stream outputStream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| outputStream | Stream | تيار الإخراج. |

## ملاحظات

يرى[`SetFontsSources`](../setfontssources/) وصف الطريقة لمزيد من المعلومات.

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

* class [FontSettings](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
