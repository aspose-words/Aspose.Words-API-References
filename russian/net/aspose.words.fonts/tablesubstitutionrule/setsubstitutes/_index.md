---
title: TableSubstitutionRule.SetSubstitutes
linktitle: SetSubstitutes
articleTitle: SetSubstitutes
second_title: Aspose.Words для .NET
description: Узнайте, как настроить названия шрифтов с помощью метода TableSubstitutionRule SetSubstitutes. Улучшите свой дизайн с помощью индивидуальных типографических решений!
type: docs
weight: 80
url: /ru/net/aspose.words.fonts/tablesubstitutionrule/setsubstitutes/
---
## TableSubstitutionRule.SetSubstitutes method

Переопределить заменяющие имена шрифтов для указанного исходного имени шрифта.

```csharp
public void SetSubstitutes(string originalFontName, params string[] substituteFontNames)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| originalFontName | String | Оригинальное название шрифта. |
| substituteFontNames | String[] | Список альтернативных названий шрифтов. |

## Примеры

Показывает, как задать правила замены шрифтов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

// Источники шрифтов по умолчанию содержат первый шрифт, используемый в документе.
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Второй шрифт, «Amethysta», недоступен.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Мы можем настроить таблицу замены шрифтов, которая определяет
// какие шрифты Aspose.Words будет использовать в качестве замены недоступным шрифтам.
// Установите два шрифта для замены для «Amethysta»: «Arvo» и «Courier New».
// Если первая замена недоступна, Aspose.Words пытается использовать вторую замену и т. д.
doc.FontSettings = new FontSettings();
doc.FontSettings.SubstitutionSettings.TableSubstitution.SetSubstitutes(
    "Amethysta", new[] {"Arvo", "Courier New"});

 // «Amethysta» недоступен, а правило замены гласит, что первым шрифтом для замены является «Arvo».
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

 // «Arvo» также недоступен, но «Courier New» доступен.
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// Выходной документ будет отображать текст, использующий шрифт «Amethysta», отформатированный с помощью «Courier New».
doc.Save(ArtifactsDir + "FontSettings.TableSubstitution.pdf");
```

Показывает, как работать с пользовательскими таблицами замены шрифтов.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Создаем новое правило подстановки таблиц и загружаем таблицу подстановки шрифтов Windows по умолчанию.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;

// Если мы выбираем шрифты исключительно из нашей папки, нам понадобится специальная таблица подстановки.
// У нас больше не будет доступа к шрифтам Microsoft Windows,
// например «Arial» или «Times New Roman», поскольку их нет в нашей новой папке шрифтов.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// Ниже приведены два способа загрузки таблицы замен из файла в локальной файловой системе.
// 1 - Из потока:
using (FileStream fileStream = new FileStream(MyDir + "Font substitution rules.xml", FileMode.Open))
{
    tableSubstitutionRule.Load(fileStream);
}

// 2 - Напрямую из файла:
tableSubstitutionRule.Load(MyDir + "Font substitution rules.xml");

// Поскольку у нас больше нет доступа к «Arial», наша таблица шрифтов сначала попытается заменить его на «Nonexistent Font».
// У нас нет этого шрифта, поэтому он будет заменен следующим заменителем, «Kreon», который находится в папке «MyFonts».
Assert.AreEqual(new[] {"Missing Font", "Kreon"}, tableSubstitutionRule.GetSubstitutes("Arial").ToArray());

// Мы можем расширить эту таблицу программно. Мы добавим запись, которая заменит "Times New Roman" на "Arvo"
Assert.Null(tableSubstitutionRule.GetSubstitutes("Times New Roman"));
tableSubstitutionRule.AddSubstitutes("Times New Roman", "Arvo");
Assert.AreEqual(new[] {"Arvo"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// Мы можем добавить вторичную резервную замену для существующей записи шрифта с помощью AddSubstitutes().
// В случае, если «Арво» недоступен, наша таблица будет искать «М+ 2м» в качестве второго варианта замены.
tableSubstitutionRule.AddSubstitutes("Times New Roman", "M+ 2m");
Assert.AreEqual(new[] {"Arvo", "M+ 2m"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// SetSubstitutes() может установить новый список заменяющих шрифтов для шрифта.
tableSubstitutionRule.SetSubstitutes("Times New Roman", "Squarish Sans CT", "M+ 2m");
Assert.AreEqual(new[] {"Squarish Sans CT", "M+ 2m"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// Написание текста шрифтами, к которым у нас нет доступа, вызовет применение наших правил подстановки.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial";
builder.Writeln("Text written in Arial, to be substituted by Kreon.");

builder.Font.Name = "Times New Roman";
builder.Writeln("Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Custom.pdf");
```

### Смотрите также

* class [TableSubstitutionRule](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
