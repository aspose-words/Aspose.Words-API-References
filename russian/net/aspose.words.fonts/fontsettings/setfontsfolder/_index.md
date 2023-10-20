---
title: FontSettings.SetFontsFolder
linktitle: SetFontsFolder
articleTitle: SetFontsFolder
second_title: Aspose.Words для .NET
description: FontSettings SetFontsFolder метод. Устанавливает папку в которой Aspose.Words ищет шрифты TrueType при рендеринге документов или встраивании шрифтов. Это ярлык дляSetFontsFolders для установки только одного каталога шрифтов на С#.
type: docs
weight: 80
url: /ru/net/aspose.words.fonts/fontsettings/setfontsfolder/
---
## FontSettings.SetFontsFolder method

Устанавливает папку, в которой Aspose.Words ищет шрифты TrueType при рендеринге документов или встраивании шрифтов. Это ярлык для[`SetFontsFolders`](../setfontsfolders/) для установки только одного каталога шрифтов.

```csharp
public void SetFontsFolder(string fontFolder, bool recursive)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fontFolder | String | Папка, содержащая шрифты TrueType. |
| recursive | Boolean | Значение true для рекурсивного сканирования указанных папок на наличие шрифтов. |

## Примеры

Показывает, как установить исходный каталог шрифта.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arvo";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Наши источники шрифтов не содержат шрифт, который мы использовали для текста в этом документе.
// Если мы используем эти настройки шрифта при рендеринге этого документа,
// Aspose.Words применит резервный шрифт к тексту, который имеет шрифт, который Aspose.Words не может найти.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// В источниках шрифтов по умолчанию отсутствуют два шрифта, которые мы используем в этом документе.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Используйте метод SetFontsFolder, чтобы установить каталог, который будет служить новым источником шрифтов.
// Передаем «false» в качестве «рекурсивного» аргумента, чтобы включить шрифты из всех файлов шрифтов, находящихся в каталоге.
// что мы передаем первый аргумент, но не включаем шрифты ни в одну из подпапок этого каталога.
// Передаем «true» в качестве «рекурсивного» аргумента, чтобы включить все файлы шрифтов в передаваемом каталоге
// в первом аргументе, а также все шрифты в его подкаталогах.
FontSettings.DefaultInstance.SetFontsFolder(FontsDir, recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Шрифт «Amethysta» находится в подпапке каталога шрифтов.
if (recursive)
{
    Assert.AreEqual(25, newFontSources[0].GetAvailableFonts().Count);
    Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
}
else
{
    Assert.AreEqual(18, newFontSources[0].GetAvailableFonts().Count);
    Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
}

doc.Save(ArtifactsDir + "FontSettings.SetFontsFolder.pdf");

// Восстанавливаем исходные источники шрифтов.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Смотрите также

* class [FontSettings](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
