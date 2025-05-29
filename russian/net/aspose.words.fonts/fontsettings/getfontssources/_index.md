---
title: FontSettings.GetFontsSources
linktitle: GetFontsSources
articleTitle: GetFontsSources
second_title: Aspose.Words для .NET
description: Откройте для себя метод FontSettings GetFontsSources для легкого доступа к массиву источников для шрифтов TrueType в Aspose.Words. Оптимизируйте управление шрифтами сегодня!
type: docs
weight: 50
url: /ru/net/aspose.words.fonts/fontsettings/getfontssources/
---
## FontSettings.GetFontsSources method

Получает копию массива, содержащего список источников, в которых Aspose.Words ищет шрифты TrueType.

```csharp
public FontSourceBase[] GetFontsSources()
```

### Возвращаемое значение

Копия текущих исходных шрифтов.

## Примечания

Возвращаемое значение является копией данных, которые использует Aspose.Words. Если вы измените entry в возвращаемом массиве, это не повлияет на рендеринг документа. Чтобы указать новый шрифт sources , используйте[`SetFontsSources`](../setfontssources/) метод.

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
