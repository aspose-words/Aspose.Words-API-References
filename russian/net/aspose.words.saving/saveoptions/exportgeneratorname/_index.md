---
title: SaveOptions.ExportGeneratorName
linktitle: ExportGeneratorName
articleTitle: ExportGeneratorName
second_title: Aspose.Words для .NET
description: Улучшите свои документы с помощью свойства SaveOptions ExportGeneratorName. Вставьте имя и версию Aspose.Words для лучшей прослеживаемости. По умолчанию — true.
type: docs
weight: 80
url: /ru/net/aspose.words.saving/saveoptions/exportgeneratorname/
---
## SaveOptions.ExportGeneratorName property

Когда`истинный` , приводит к внедрению имени и версии Aspose.Words в создаваемые файлы. Значение по умолчанию:`истинный` .

```csharp
public bool ExportGeneratorName { get; set; }
```

## Примеры

Показывает, как отключить добавление имени и версии Aspose.Words в создаваемые файлы.

```csharp
Document doc = new Document();

// Используйте https://docs.aspose.com/words/net/generator-or-producer-name-included-in-output-documents/, чтобы узнать, как проверить результат.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { ExportGeneratorName = false };

doc.Save(ArtifactsDir + "OoxmlSaveOptions.ExportGeneratorName.docx", saveOptions);
```

### Смотрите также

* class [SaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
