---
title: FontSettings.SetFontsSources
linktitle: SetFontsSources
articleTitle: SetFontsSources
second_title: Aspose.Words для .NET
description: Узнайте, как метод SetFontsSources в Aspose.Words улучшает визуализацию документов, указывая источники шрифтов TrueType для достижения оптимальных результатов.
type: docs
weight: 100
url: /ru/net/aspose.words.fonts/fontsettings/setfontssources/
---
## SetFontsSources(*FontSourceBase[]*) {#setfontssources}

Устанавливает источники, в которых Aspose.Words ищет шрифты TrueType при рендеринге документов или внедрении шрифтов.

```csharp
public void SetFontsSources(FontSourceBase[] sources)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| sources | FontSourceBase[] | Массив источников, содержащих шрифты TrueType. |

## Примечания

По умолчанию Aspose.Words ищет шрифты, установленные в системе.

Установка этого свойства сбрасывает кэш всех ранее загруженных шрифтов.

## Примеры

Показывает, как добавить источник шрифтов к существующим источникам шрифтов.

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

// В источнике шрифтов по умолчанию отсутствуют два шрифта, которые мы используем в нашем документе.
// При сохранении этого документа Aspose.Words применит резервные шрифты ко всему тексту, отформатированному недоступными шрифтами.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Создаем источник шрифтов из папки, содержащей шрифты.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// Применяем новый массив источников шрифтов, содержащий исходные источники шрифтов, а также наши пользовательские шрифты.
FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
FontSettings.DefaultInstance.SetFontsSources(updatedFontSources);

// Убедитесь, что Aspose.Words имеет доступ ко всем необходимым шрифтам, прежде чем преобразовывать документ в PDF.
updatedFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.True(updatedFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

doc.Save(ArtifactsDir + "FontSettings.AddFontSource.pdf");

// Восстановить исходные источники шрифтов.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Смотрите также

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)

---

## SetFontsSources(*FontSourceBase[], Stream*) {#setfontssources_1}

Устанавливает источники, в которых Aspose.Words ищет шрифты TrueType, и дополнительно загружает ранее сохраненный кэш поиска шрифтов.

```csharp
public void SetFontsSources(FontSourceBase[] sources, Stream cacheInputStream)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| sources | FontSourceBase[] | Массив источников, содержащих шрифты TrueType. |
| cacheInputStream | Stream | Входной поток с сохраненным кэшем поиска шрифтов. |

## Примечания

Загрузка ранее сохраненного кэша поиска шрифтов ускорит процесс инициализации кэша шрифтов. Это особенно полезно, когда доступ к источникам шрифтов затруднен (например, когда шрифты загружаются по сети).

При сохранении и загрузке кэша поиска шрифтов шрифты в предоставленных источниках идентифицируются с помощью ключа кэша. Для шрифтов в[`SystemFontSource`](../../systemfontsource/) и[`FolderFontSource`](../../folderfontsource/) Ключ кэша — это path к файлу шрифта. Для[`MemoryFontSource`](../../memoryfontsource/) и[`StreamFontSource`](../../streamfontsource/)Ключ кэша определен в[`CacheKey`](../../memoryfontsource/cachekey/) и[`CacheKey`](../../streamfontsource/cachekey/) properties соответственно. Для[`FileFontSource`](../../filefontsource/) ключ кэша — это либо[`CacheKey`](../../filefontsource/cachekey/) Свойство или путь к файлу, если[`CacheKey`](../../filefontsource/cachekey/) является`нулевой`.

Настоятельно рекомендуется при загрузке кэша указывать те же источники шрифтов, что и на момент сохранения кэша. Любые изменения в источниках шрифтов (например, добавление новых шрифтов, перемещение файлов шрифтов или изменение ключа кэша) могут привести к неточному разрешению шрифтов Aspose.Words.

## Примеры

Показывает, как ускорить процесс инициализации кэша шрифтов.

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
/// Загружать данные шрифта только при необходимости, а не сохранять их в памяти
/// на все время существования объекта "FontSettings".
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

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
