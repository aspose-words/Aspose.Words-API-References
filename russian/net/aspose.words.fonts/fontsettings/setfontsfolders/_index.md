---
title: FontSettings.SetFontsFolders
linktitle: SetFontsFolders
articleTitle: SetFontsFolders
second_title: Aspose.Words для .NET
description: FontSettings SetFontsFolders метод. Устанавливает папки в которых Aspose.Words ищет шрифты TrueType при рендеринге документов или встраивании шрифтов на С#.
type: docs
weight: 90
url: /ru/net/aspose.words.fonts/fontsettings/setfontsfolders/
---
## FontSettings.SetFontsFolders method

Устанавливает папки, в которых Aspose.Words ищет шрифты TrueType при рендеринге документов или встраивании шрифтов.

```csharp
public void SetFontsFolders(string[] fontsFolders, bool recursive)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fontsFolders | String[] | Массив папок, содержащих шрифты TrueType. |
| recursive | Boolean | Значение true для рекурсивного сканирования указанных папок на наличие шрифтов. |

## Примечания

По умолчанию Aspose.Words ищет шрифты, установленные в системе.

Установка этого свойства сбрасывает кеш всех ранее загруженных шрифтов.

## Примеры

Показывает, как установить несколько исходных каталогов шрифтов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Наши источники шрифтов не содержат шрифт, который мы использовали для текста в этом документе.
// Если мы используем эти настройки шрифта при рендеринге этого документа,
// Aspose.Words применит резервный шрифт к тексту, который имеет шрифт, который Aspose.Words не может найти.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// В источниках шрифтов по умолчанию отсутствуют два шрифта, которые мы используем в этом документе.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Используйте метод SetFontsFolders для создания источника шрифта из каждого каталога шрифтов, который мы передаем в качестве первого аргумента.
// Передаем «false» в качестве «рекурсивного» аргумента, чтобы включить шрифты из всех файлов шрифтов, находящихся в каталогах
// что мы передаем первый аргумент, но не включаем шрифты из каких-либо подпапок каталогов.
// Передаем «true» в качестве «рекурсивного» аргумента, чтобы включить все файлы шрифтов в передаваемые каталоги
// в первом аргументе, а также все шрифты в их подкаталогах.
FontSettings.DefaultInstance.SetFontsFolders(new[] {FontsDir + "/Amethysta", FontsDir + "/Junction"},
    recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(2, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.AreEqual(1, newFontSources[0].GetAvailableFonts().Count);
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Сама папка «Junction» не содержит файлов шрифтов, но имеет подпапки, которые содержат.
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

// Восстанавливаем исходные источники шрифтов.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Смотрите также

* class [FontSettings](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
