---
title: ImportFormatOptions.IgnoreHeaderFooter
linktitle: IgnoreHeaderFooter
articleTitle: IgnoreHeaderFooter
second_title: Aspose.Words для .NET
description: ImportFormatOptions IgnoreHeaderFooter свойство. Получает или задает логическое значение указывающее что исходное форматирование содержимого верхних и нижних колонтитулов игнорируется  еслиKeepSourceFormatting используется режим. Значение по умолчаниюистинный  на С#.
type: docs
weight: 40
url: /ru/net/aspose.words/importformatoptions/ignoreheaderfooter/
---
## ImportFormatOptions.IgnoreHeaderFooter property

Получает или задает логическое значение, указывающее, что исходное форматирование содержимого верхних и нижних колонтитулов игнорируется , еслиKeepSourceFormatting используется режим. Значение по умолчанию:`истинный` .

```csharp
public bool IgnoreHeaderFooter { get; set; }
```

## Примеры

Показывает, как указать игнорирование или отсутствие исходного форматирования содержимого верхних и нижних колонтитулов.

```csharp
Document dstDoc = new Document(MyDir + "Document.docx");
Document srcDoc = new Document(MyDir + "Header and footer types.docx");

ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreHeaderFooter = false;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, importFormatOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

### Смотрите также

* class [ImportFormatOptions](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
