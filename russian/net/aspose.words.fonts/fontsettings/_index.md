---
title: FontSettings Class
linktitle: FontSettings
articleTitle: FontSettings
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fonts.FontSettings, чтобы легко настраивать параметры шрифтов документа для повышения его читабельности и профессиональной презентации.
type: docs
weight: 3400
url: /ru/net/aspose.words.fonts/fontsettings/
---
## FontSettings class

Задает настройки шрифта для документа.

Чтобы узнать больше, посетите[Работа со шрифтами](https://docs.aspose.com/words/net/working-with-fonts/) документальная статья.

```csharp
public class FontSettings
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FontSettings](fontsettings/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| static [DefaultInstance](../../aspose.words.fonts/fontsettings/defaultinstance/) { get; } | Статические настройки шрифта по умолчанию. |
| [FallbackSettings](../../aspose.words.fonts/fontsettings/fallbacksettings/) { get; } | Настройки, связанные с механизмом резервного копирования шрифтов. |
| [SubstitutionSettings](../../aspose.words.fonts/fontsettings/substitutionsettings/) { get; } | Настройки, связанные с механизмом замены шрифтов. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFontsSources](../../aspose.words.fonts/fontsettings/getfontssources/)() | Получает копию массива, содержащего список источников, в которых Aspose.Words ищет шрифты TrueType. |
| [ResetFontSources](../../aspose.words.fonts/fontsettings/resetfontsources/)() | Сбрасывает источники шрифтов до системных значений по умолчанию. |
| [SaveSearchCache](../../aspose.words.fonts/fontsettings/savesearchcache/)(*Stream*) | Сохраняет кэш поиска шрифтов в потоке. |
| [SetFontsFolder](../../aspose.words.fonts/fontsettings/setfontsfolder/)(*string, bool*) | Задает папку, в которой Aspose.Words ищет шрифты TrueType при рендеринге документов или внедрении шрифтов. Это ярлык для[`SetFontsFolders`](./setfontsfolders/) для установки только одного каталога шрифтов. |
| [SetFontsFolders](../../aspose.words.fonts/fontsettings/setfontsfolders/)(*string[], bool*) | Устанавливает папки, в которых Aspose.Words ищет шрифты TrueType при рендеринге документов или внедрении шрифтов. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources/#setfontssources)(*FontSourceBase[]*) | Устанавливает источники, в которых Aspose.Words ищет шрифты TrueType при рендеринге документов или внедрении шрифтов. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources/#setfontssources_1)(*FontSourceBase[], Stream*) | Устанавливает источники, в которых Aspose.Words ищет шрифты TrueType, и дополнительно загружает ранее сохраненный кэш поиска шрифтов. |

## Примечания

Aspose.Words использует настройки шрифтов для разрешения шрифтов в документе. Шрифты разрешаются в основном при построении макета документа или рендеринге в фиксированные форматы страниц. Но при загрузке некоторых форматов Aspose.Words также может потребовать разрешения шрифтов. Например, когда загружаются документы HTML Aspose.Words может разрешить шрифты для выполнения резервного копирования шрифтов. Поэтому рекомендуется задать настройки шрифтов в [`LoadOptions`](../../aspose.words.loading/loadoptions/) при загрузке документа. Или, по крайней мере, перед построением макета или преобразованием документа в формат с фиксированной страницей.

По умолчанию все документы используют один экземпляр статических настроек шрифта. Доступ к нему можно получить по [`DefaultInstance`](./defaultinstance/) свойство.

Изменение настроек шрифта безопасно в любое время из любого потока. Но рекомендуется не менять настройки шрифта while при обработке некоторых документов, использующих эти настройки. Это может привести к тому, что один и тот же шрифт будет разрешен по-разному в разных частях документа.

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

Показывает, как задать исходный каталог шрифтов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arvo";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Наши источники шрифтов не содержат шрифт, который мы использовали для текста в этом документе.
// Если мы используем эти настройки шрифта при рендеринге этого документа,
// Aspose.Words применит резервный шрифт к тексту, шрифт которого Aspose.Words не может найти.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// В источниках шрифтов по умолчанию отсутствуют два шрифта, которые мы используем в этом документе.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Используйте метод «SetFontsFolder», чтобы задать каталог, который будет выступать в качестве нового источника шрифтов.
// Передайте «false» как «рекурсивный» аргумент, чтобы включить шрифты из всех файлов шрифтов, которые находятся в каталоге
// который мы передаем в первом аргументе, но не включаем никакие шрифты ни в одну из подпапок этого каталога.
// Передайте «true» как «рекурсивный» аргумент, чтобы включить все файлы шрифтов в каталоге, который мы передаем
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

// Восстановить исходные источники шрифтов.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

Показывает, как задать несколько исходных каталогов шрифтов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Наши источники шрифтов не содержат шрифт, который мы использовали для текста в этом документе.
// Если мы используем эти настройки шрифта при рендеринге этого документа,
// Aspose.Words применит резервный шрифт к тексту, шрифт которого Aspose.Words не может найти.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// В источниках шрифтов по умолчанию отсутствуют два шрифта, которые мы используем в этом документе.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Используйте метод «SetFontsFolders» для создания источника шрифта из каждого каталога шрифтов, который мы передаем в качестве первого аргумента.
// Передайте «false» как «рекурсивный» аргумент, чтобы включить шрифты из всех файлов шрифтов, которые находятся в каталогах
// который мы передаем в первом аргументе, но не включаем никакие шрифты из подпапок каталогов.
// Передайте «true» как «рекурсивный» аргумент, чтобы включить все файлы шрифтов в каталогах, которые мы передаем
// в первом аргументе, а также все шрифты в их подкаталогах.
FontSettings.DefaultInstance.SetFontsFolders(new[] {FontsDir + "/Amethysta", FontsDir + "/Junction"},
    recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(2, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.AreEqual(1, newFontSources[0].GetAvailableFonts().Count);
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Сама папка «Junction» не содержит файлов шрифтов, но имеет подпапки, в которых они есть.
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

// Восстановить исходные источники шрифтов.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Смотрите также

* пространство имен [Aspose.Words.Fonts](../../aspose.words.fonts/)
* сборка [Aspose.Words](../../)
