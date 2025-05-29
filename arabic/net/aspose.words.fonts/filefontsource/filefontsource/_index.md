---
title: FileFontSource
linktitle: FileFontSource
articleTitle: FileFontSource
second_title: Aspose.Words لـ .NET
description: اكتشف مُنشئ FileFontSource لدمج الخطوط بسلاسة في مشاريعك. حسّن تصميمك بحلول برمجة سهلة الاستخدام!
type: docs
weight: 10
url: /ar/net/aspose.words.fonts/filefontsource/filefontsource/
---
## FileFontSource(*string*) {#constructor}

المولد.

```csharp
public FileFontSource(string filePath)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| filePath | String | المسار إلى ملف الخط. |

## أمثلة

يوضح كيفية استخدام ملف الخط في نظام الملفات المحلي كمصدر للخط.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### أنظر أيضا

* class [FileFontSource](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)

---

## FileFontSource(*string, int*) {#constructor_1}

المولد.

```csharp
public FileFontSource(string filePath, int priority)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| filePath | String | المسار إلى ملف الخط. |
| priority | Int32 | أولوية مصدر الخط. انظر[`Priority`](../../fontsourcebase/priority/) وصف العقار لمزيد من المعلومات. |

## أمثلة

يوضح كيفية استخدام ملف الخط في نظام الملفات المحلي كمصدر للخط.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### أنظر أيضا

* class [FileFontSource](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)

---

## FileFontSource(*string, int, string*) {#constructor_2}

المولد.

```csharp
public FileFontSource(string filePath, int priority, string cacheKey)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| filePath | String | المسار إلى ملف الخط. |
| priority | Int32 | أولوية مصدر الخط. انظر[`Priority`](../../fontsourcebase/priority/) وصف العقار لمزيد من المعلومات. |
| cacheKey | String | مفتاح هذا المصدر في ذاكرة التخزين المؤقت. انظر[`CacheKey`](../cachekey/) وصف العقار لمزيد من المعلومات. |

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

* class [FileFontSource](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
