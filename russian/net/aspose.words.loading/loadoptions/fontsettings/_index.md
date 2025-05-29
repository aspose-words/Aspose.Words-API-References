---
title: LoadOptions.FontSettings
linktitle: FontSettings
articleTitle: FontSettings
second_title: Aspose.Words для .NET
description: Настройте параметры шрифта вашего документа с помощью LoadOptions FontSettings для улучшения читаемости и стиля. Оптимизируйте свои документы без усилий!
type: docs
weight: 60
url: /ru/net/aspose.words.loading/loadoptions/fontsettings/
---
## LoadOptions.FontSettings property

Позволяет указать настройки шрифта документа.

```csharp
public FontSettings FontSettings { get; set; }
```

## Примечания

При загрузке некоторых форматов Aspose.Words может потребовать разрешить шрифты. Например, при загрузке HTML-документов Aspose.Words может разрешить шрифты для выполнения резервного копирования шрифтов.

Если установлено значение`нулевой` , настройки статического шрифта по умолчанию[`DefaultInstance`](../../../aspose.words.fonts/fontsettings/defaultinstance/) будет использоваться.

Значение по умолчанию:`нулевой`.

## Примеры

Показывает, как применять настройки замены шрифтов при загрузке документа.

```csharp
// Создаем объект FontSettings, который заменит шрифт "Times New Roman"
// со шрифтом "Arvo" из нашей папки "MyFonts".
FontSettings fontSettings = new FontSettings();
fontSettings.SetFontsFolder(FontsDir, false);
fontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Times New Roman", "Arvo");

// Установите объект FontSettings как свойство вновь созданного объекта LoadOptions.
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = fontSettings;

// Загружаем документ, затем преобразуем его в PDF-файл с заменой шрифта.
Document doc = new Document(MyDir + "Document.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.FontSettings.pdf");
```

Показывает, как назначать замену шрифтов во время загрузки.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = new FontSettings();

// Устанавливаем правило замены шрифта для объекта LoadOptions.
// Если загружаемый нами документ использует шрифт, которого у нас нет,
// это правило заменит недоступный шрифт на существующий.
// В этом случае все использования «MissingFont» будут преобразованы в «Comic Sans MS».
TableSubstitutionRule substitutionRule = loadOptions.FontSettings.SubstitutionSettings.TableSubstitution;
substitutionRule.AddSubstitutes("MissingFont", "Comic Sans MS");

Document doc = new Document(MyDir + "Missing font.html", loadOptions);

// На этом этапе такой текст все еще будет в «MissingFont».
// Замена шрифта произойдет при рендеринге документа.
Assert.AreEqual("MissingFont", doc.FirstSection.Body.FirstParagraph.Runs[0].Font.Name);

doc.Save(ArtifactsDir + "FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
```

### Смотрите также

* class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* class [LoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
