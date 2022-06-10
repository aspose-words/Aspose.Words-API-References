---
title: Load
second_title: Справочник по API Aspose.Words для .NET
description: Загружает настройки подстановки таблиц из файла XML.
type: docs
weight: 30
url: /ru/net/aspose.words.fonts/tablesubstitutionrule/load/
---
## Load(string) {#load_1}

Загружает настройки подстановки таблиц из файла XML.

```csharp
public void Load(string fileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Введите имя файла. |

### Примеры

Показывает, как работать с пользовательскими таблицами замены шрифтов.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Создать новое правило подстановки таблиц и загрузить таблицу подстановки шрифтов Windows по умолчанию.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;

// Если мы будем выбирать шрифты исключительно из нашей папки, нам понадобится пользовательская таблица подстановки.
// У нас больше не будет доступа к шрифтам Microsoft Windows,
// такие как «Arial» или «Times New Roman», так как их нет в нашей новой папке шрифтов.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// Ниже приведены два способа загрузки таблицы замещения из файла в локальной файловой системе.
// 1 - Из потока:
using (FileStream fileStream = new FileStream(MyDir + "Font substitution rules.xml", FileMode.Open))
{
    tableSubstitutionRule.Load(fileStream);
}

// 2 - Напрямую из файла:
tableSubstitutionRule.Load(MyDir + "Font substitution rules.xml");

// Поскольку у нас больше нет доступа к «Arial», наша таблица шрифтов сначала попытается заменить его на «Nonexistent Font».
// У нас нет этого шрифта, поэтому он переместится на следующую замену, "Kreon", найденную в папке "MyFonts".
Assert.AreEqual(new[] {"Missing Font", "Kreon"}, tableSubstitutionRule.GetSubstitutes("Arial").ToArray());

// Мы можем расширить эту таблицу программно. Мы добавим запись, которая заменяет «Times New Roman» на «Arvo».
Assert.Null(tableSubstitutionRule.GetSubstitutes("Times New Roman"));
tableSubstitutionRule.AddSubstitutes("Times New Roman", "Arvo");
Assert.AreEqual(new[] {"Arvo"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// Мы можем добавить вторичную резервную замену для существующей записи шрифта с помощью AddSubstitutes().
// Если "Arvo" недоступен, наша таблица будет искать "M+ 2m" в качестве второго варианта замены.
tableSubstitutionRule.AddSubstitutes("Times New Roman", "M+ 2m");
Assert.AreEqual(new[] {"Arvo", "M+ 2m"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// SetSubstitutes() может установить новый список шрифтов-заменителей для шрифта.
tableSubstitutionRule.SetSubstitutes("Times New Roman", new[] {"Squarish Sans CT", "M+ 2m"});
Assert.AreEqual(new[] {"Squarish Sans CT", "M+ 2m"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// Написание текста шрифтами, к которым у нас нет доступа, вызовет наши правила подстановки.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial";
builder.Writeln("Text written in Arial, to be substituted by Kreon.");

builder.Font.Name = "Times New Roman";
builder.Writeln("Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Custom.pdf");
```

### Смотрите также

* class [TableSubstitutionRule](../../tablesubstitutionrule)
* пространство имен [Aspose.Words.Fonts](../../tablesubstitutionrule)
* сборка [Aspose.Words](../../../)

---

## Load(Stream) {#load}

Загружает настройки подстановки таблиц из XML-потока.

```csharp
public void Load(Stream stream)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Входной поток. |

### Примеры

Показывает, как работать с пользовательскими таблицами замены шрифтов.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Создать новое правило подстановки таблиц и загрузить таблицу подстановки шрифтов Windows по умолчанию.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;

// Если мы будем выбирать шрифты исключительно из нашей папки, нам понадобится пользовательская таблица подстановки.
// У нас больше не будет доступа к шрифтам Microsoft Windows,
// такие как «Arial» или «Times New Roman», так как их нет в нашей новой папке шрифтов.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// Ниже приведены два способа загрузки таблицы замещения из файла в локальной файловой системе.
// 1 - Из потока:
using (FileStream fileStream = new FileStream(MyDir + "Font substitution rules.xml", FileMode.Open))
{
    tableSubstitutionRule.Load(fileStream);
}

// 2 - Напрямую из файла:
tableSubstitutionRule.Load(MyDir + "Font substitution rules.xml");

// Поскольку у нас больше нет доступа к «Arial», наша таблица шрифтов сначала попытается заменить его на «Nonexistent Font».
// У нас нет этого шрифта, поэтому он переместится на следующую замену, "Kreon", найденную в папке "MyFonts".
Assert.AreEqual(new[] {"Missing Font", "Kreon"}, tableSubstitutionRule.GetSubstitutes("Arial").ToArray());

// Мы можем расширить эту таблицу программно. Мы добавим запись, которая заменяет «Times New Roman» на «Arvo».
Assert.Null(tableSubstitutionRule.GetSubstitutes("Times New Roman"));
tableSubstitutionRule.AddSubstitutes("Times New Roman", "Arvo");
Assert.AreEqual(new[] {"Arvo"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// Мы можем добавить вторичную резервную замену для существующей записи шрифта с помощью AddSubstitutes().
// Если "Arvo" недоступен, наша таблица будет искать "M+ 2m" в качестве второго варианта замены.
tableSubstitutionRule.AddSubstitutes("Times New Roman", "M+ 2m");
Assert.AreEqual(new[] {"Arvo", "M+ 2m"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// SetSubstitutes() может установить новый список шрифтов-заменителей для шрифта.
tableSubstitutionRule.SetSubstitutes("Times New Roman", new[] {"Squarish Sans CT", "M+ 2m"});
Assert.AreEqual(new[] {"Squarish Sans CT", "M+ 2m"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// Написание текста шрифтами, к которым у нас нет доступа, вызовет наши правила подстановки.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial";
builder.Writeln("Text written in Arial, to be substituted by Kreon.");

builder.Font.Name = "Times New Roman";
builder.Writeln("Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Custom.pdf");
```

### Смотрите также

* class [TableSubstitutionRule](../../tablesubstitutionrule)
* пространство имен [Aspose.Words.Fonts](../../tablesubstitutionrule)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
