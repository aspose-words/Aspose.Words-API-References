---
title: LoadOptions.FontSettings
second_title: Справочник по API Aspose.Words для .NET
description: LoadOptions свойство. Позволяет указать настройки шрифта документа.
type: docs
weight: 60
url: /ru/net/aspose.words.loading/loadoptions/fontsettings/
---
## LoadOptions.FontSettings property

Позволяет указать настройки шрифта документа.

```csharp
public FontSettings FontSettings { get; set; }
```

### Примечания

При загрузке некоторых форматов Aspose.Words может потребоваться разрешить шрифты. Например, при загрузке HTML-документов Aspose.Words может разрешить шрифты для выполнения резервного шрифта.

Если установлено значение`нулевой` , настройки статического шрифта по умолчанию[`DefaultInstance`](../../../aspose.words.fonts/fontsettings/defaultinstance/) будет использован.

Значение по умолчанию:`нулевой`.

### Примеры

Показывает, как применить настройки подстановки шрифтов при загрузке документа.

```csharp
// Создаем объект FontSettings, который заменит шрифт Times New Roman.
// со шрифтом «Arvo» из нашей папки «MyFonts».
FontSettings fontSettings = new FontSettings();
fontSettings.SetFontsFolder(FontsDir, false);
fontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Times New Roman", "Arvo");

// Установите этот объект FontSettings как свойство вновь созданного объекта LoadOptions.
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = fontSettings;

// Загрузите документ, затем отобразите его в формате PDF с заменой шрифта.
Document doc = new Document(MyDir + "Document.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.FontSettings.pdf");
```

Показывает, как назначать заменители шрифтов во время загрузки.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = new FontSettings();

// Устанавливаем правило подстановки шрифта для объекта LoadOptions.
// Если в загружаемом документе используется шрифт, которого у нас нет,
// это правило заменит недоступный шрифт существующим.
// В этом случае все варианты использования «MissingFont» будут преобразованы в «Comic Sans MS».
TableSubstitutionRule substitutionRule = loadOptions.FontSettings.SubstitutionSettings.TableSubstitution;
substitutionRule.AddSubstitutes("MissingFont", new[] {"Comic Sans MS"});

Document doc = new Document(MyDir + "Missing font.html", loadOptions);

// На этом этапе такой текст все еще будет в «MissingFont».
// Замена шрифта произойдет при рендеринге документа.
Assert.AreEqual("MissingFont", doc.FirstSection.Body.FirstParagraph.Runs[0].Font.Name);

doc.Save(ArtifactsDir + "FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
```

### Смотрите также

* class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* class [LoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../loadoptions/)
* сборка [Aspose.Words](../../../)


