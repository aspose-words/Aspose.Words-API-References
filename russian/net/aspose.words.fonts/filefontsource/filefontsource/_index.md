---
title: FileFontSource.FileFontSource
second_title: Справочник по API Aspose.Words для .NET
description: FileFontSource строитель. Стор.
type: docs
weight: 10
url: /ru/net/aspose.words.fonts/filefontsource/filefontsource/
---
## FileFontSource(string) {#constructor}

Стор.

```csharp
public FileFontSource(string filePath)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| filePath | String | Путь к файлу шрифта. |

### Примеры

Показывает, как использовать файл шрифта в локальной файловой системе в качестве источника шрифта.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### Смотрите также

* class [FileFontSource](../)
* пространство имен [Aspose.Words.Fonts](../../filefontsource/)
* сборка [Aspose.Words](../../../)

---

## FileFontSource(string, int) {#constructor_1}

Стор.

```csharp
public FileFontSource(string filePath, int priority)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| filePath | String | Путь к файлу шрифта. |
| priority | Int32 | Приоритет источника шрифта. См.[`Priority`](../../fontsourcebase/priority/) описание свойства для получения дополнительной информации. |

### Примеры

Показывает, как использовать файл шрифта в локальной файловой системе в качестве источника шрифта.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### Смотрите также

* class [FileFontSource](../)
* пространство имен [Aspose.Words.Fonts](../../filefontsource/)
* сборка [Aspose.Words](../../../)

---

## FileFontSource(string, int, string) {#constructor_2}

Стор.

```csharp
public FileFontSource(string filePath, int priority, string cacheKey)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| filePath | String | Путь к файлу шрифта. |
| priority | Int32 | Приоритет источника шрифта. См.[`Priority`](../../fontsourcebase/priority/) описание свойства для получения дополнительной информации. |
| cacheKey | String | Ключ этого источника в кеше. Видеть[`CacheKey`](../cachekey/) описание свойства для получения дополнительной информации. |

### Примеры

Показывает, как ускорить процесс инициализации кэша шрифтов.

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
/// Загружаем данные шрифта только при необходимости, а не сохраняем их в памяти
/// на все время жизни объекта FontSettings.
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

### Смотрите также

* class [FileFontSource](../)
* пространство имен [Aspose.Words.Fonts](../../filefontsource/)
* сборка [Aspose.Words](../../../)


