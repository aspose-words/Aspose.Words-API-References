---
title: PclSaveOptions.FallbackFontName
linktitle: FallbackFontName
articleTitle: FallbackFontName
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PclSaveOptions FallbackFontName, обеспечивающее бесперебойную печать со шрифтом по умолчанию, когда нужный вам шрифт недоступен.
type: docs
weight: 20
url: /ru/net/aspose.words.saving/pclsaveoptions/fallbackfontname/
---
## PclSaveOptions.FallbackFontName property

Имя шрифта, который будет использоваться , если ожидаемый шрифт не найден в коллекциях принтера и встроенных шрифтов.

```csharp
public string FallbackFontName { get; set; }
```

## Примечания

Если резервный вариант не найден, выдается предупреждение и используется шрифт «Arial».

## Примеры

Показывает, как объявить шрифт, который принтер будет применять к печатному тексту в качестве замены, если исходный шрифт окажется недоступен.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.FallbackFontName = "Times New Roman";

// Этот документ даст указание принтеру применить «Times New Roman» к тексту с отсутствующим шрифтом.
// Если шрифт «Times New Roman» также недоступен, принтер по умолчанию будет использовать шрифт «Arial».
doc.Save(ArtifactsDir + "PclSaveOptions.SetPrinterFont.pcl", saveOptions);
```

### Смотрите также

* class [PclSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
