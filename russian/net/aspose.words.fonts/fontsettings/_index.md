---
title: Class FontSettings
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Fonts.FontSettings сорт. Задает настройки шрифта для документа.
type: docs
weight: 2790
url: /ru/net/aspose.words.fonts/fontsettings/
---
## FontSettings class

Задает настройки шрифта для документа.

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
| [FallbackSettings](../../aspose.words.fonts/fontsettings/fallbacksettings/) { get; } | Настройки, связанные с резервным механизмом шрифта. |
| [SubstitutionSettings](../../aspose.words.fonts/fontsettings/substitutionsettings/) { get; } | Настройки, связанные с механизмом замены шрифта. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFontsSources](../../aspose.words.fonts/fontsettings/getfontssources/)() | Получает копию массива, содержащего список источников, в которых Aspose.Words ищет шрифты TrueType. |
| [ResetFontSources](../../aspose.words.fonts/fontsettings/resetfontsources/)() | Сбрасывает источники шрифтов к системным значениям по умолчанию. |
| [SaveSearchCache](../../aspose.words.fonts/fontsettings/savesearchcache/)(Stream) | Сохраняет кеш поиска шрифтов в поток. |
| [SetFontsFolder](../../aspose.words.fonts/fontsettings/setfontsfolder/)(string, bool) | Устанавливает папку, в которой Aspose.Words ищет шрифты TrueType при рендеринге документов или встраивании шрифтов. Это ярлык для[`SetFontsFolders`](./setfontsfolders/) для установки только одного каталога шрифтов. |
| [SetFontsFolders](../../aspose.words.fonts/fontsettings/setfontsfolders/)(string[], bool) | Устанавливает папки, в которых Aspose.Words ищет шрифты TrueType при рендеринге документов или внедрении шрифтов. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources/#setfontssources)(FontSourceBase[]) | Устанавливает источники, в которых Aspose.Words ищет шрифты TrueType при отображении документов или внедрении шрифтов. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources/#setfontssources_1)(FontSourceBase[], Stream) | Устанавливает источники, в которых Aspose.Words ищет шрифты TrueType и дополнительно загружает ранее сохраненный кэш поиска шрифтов. |

### Примечания

Aspose.Words использует настройки шрифта для разрешения шрифтов в документе. Шрифты разрешаются в основном при построении документа layout или рендеринге в фиксированные форматы страниц. Но при загрузке некоторых форматов Aspose.Words также может потребовать разрешения шрифтов. Например, когда загружаются HTML-документы, Aspose.Words может разрешать шрифты для выполнения резервного шрифта. Поэтому рекомендуется установить настройки шрифта в [`LoadOptions`](../../aspose.words.loading/loadoptions/) при загрузке документа. Или, по крайней мере, перед созданием макета или рендерингом документа в формате фиксированной страницы.

По умолчанию во всех документах используется один экземпляр настроек статического шрифта. Доступ к нему мог получить [`DefaultInstance`](./defaultinstance/) имущество.

Изменение настроек шрифта безопасно в любое время из любой темы. Но рекомендуется не изменять настройки шрифта при обработке некоторых документов, в которых используются эти настройки. Это может привести к тому, что один и тот же шрифт будет разрешаться по-разному в разных частях документа.

### Примеры

Показывает, как добавить источник шрифта к нашим существующим источникам шрифтов.

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

// В источнике шрифта по умолчанию отсутствуют два шрифта, которые мы используем в нашем документе.
// Когда мы сохраним этот документ, Aspose.Words применит резервные шрифты ко всему тексту, отформатированному с использованием недоступных шрифтов.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Создаем источник шрифта из папки, содержащей шрифты.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// Применить новый массив источников шрифтов, который содержит исходные источники шрифтов, а также наши пользовательские шрифты.
FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
FontSettings.DefaultInstance.SetFontsSources(updatedFontSources);

// Убедитесь, что Aspose.Words имеет доступ ко всем необходимым шрифтам, прежде чем мы преобразуем документ в PDF.
updatedFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.True(updatedFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

doc.Save(ArtifactsDir + "FontSettings.AddFontSource.pdf");

// Восстановить исходные источники шрифтов.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

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
// Aspose.Words применит резервный шрифт к тексту, шрифт которого Aspose.Words не может найти.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// В источниках шрифтов по умолчанию отсутствуют два шрифта, которые мы используем в этом документе.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Используйте метод "SetFontsFolder", чтобы установить каталог, который будет действовать как новый источник шрифта.
// Передайте «false» в качестве «рекурсивного» аргумента, чтобы включить шрифты из всех файлов шрифтов, которые находятся в каталоге
// которые мы передаем в первом аргументе, но не включаем шрифты ни в одну из подпапок этого каталога.
// Передаем «true» в качестве «рекурсивного» аргумента, чтобы включить все файлы шрифтов в каталоге, который мы передаем
// в первом аргументе, а также все шрифты в его подкаталогах.
FontSettings.DefaultInstance.SetFontsFolder(FontsDir, recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Шрифт "Amethysta" находится в подпапке каталога шрифтов.
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
// Aspose.Words применит резервный шрифт к тексту, шрифт которого Aspose.Words не может найти.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// В источниках шрифтов по умолчанию отсутствуют два шрифта, которые мы используем в этом документе.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Используйте метод "SetFontsFolders" для создания источника шрифта из каждого каталога шрифтов, который мы передаем в качестве первого аргумента.
// Передайте «false» в качестве «рекурсивного» аргумента, чтобы включить шрифты из всех файлов шрифтов, которые находятся в каталогах
// который мы передаем в первом аргументе, но не включаем никаких шрифтов ни в одной из подпапок каталогов.
// Передаем «true» в качестве «рекурсивного» аргумента, чтобы включить все файлы шрифтов в каталогах, которые мы передаем
// в первом аргументе, а также все шрифты в их подкаталогах.
FontSettings.DefaultInstance.SetFontsFolders(new[] {FontsDir + "/Amethysta", FontsDir + "/Junction"},
    recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(2, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.AreEqual(1, newFontSources[0].GetAvailableFonts().Count);
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Сама папка "Junction" не содержит файлов шрифтов, но содержит вложенные папки.
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


