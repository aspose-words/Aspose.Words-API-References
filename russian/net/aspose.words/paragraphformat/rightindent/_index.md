---
title: RightIndent
second_title: Справочник по API Aspose.Words для .NET
description: Получает или задает значение в пунктах представляющее правый отступ для абзаца.
type: docs
weight: 260
url: /ru/net/aspose.words/paragraphformat/rightindent/
---
## ParagraphFormat.RightIndent property

Получает или задает значение (в пунктах), представляющее правый отступ для абзаца.

```csharp
public double RightIndent { get; set; }
```

### Примеры

Показывает, как настроить форматирование абзаца для создания смещенного от центра текста.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Центрируем весь текст, который пишет конструктор документов, и устанавливаем отступы.
// Приведенная ниже конфигурация отступа создаст основной текст, который будет располагаться на странице асимметрично.
// «Центр», по которому мы выравниваем текст, будет серединой основного текста, а не серединой страницы.
ParagraphFormat paragraphFormat = builder.ParagraphFormat;
paragraphFormat.Alignment = ParagraphAlignment.Center;
paragraphFormat.LeftIndent = 100;
paragraphFormat.RightIndent = 50;
paragraphFormat.SpaceAfter = 25;

builder.Writeln(
    "This paragraph demonstrates how left and right indentation affects word wrapping.");
builder.Writeln(
    "The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

doc.Save(ArtifactsDir + "DocumentBuilder.SetParagraphFormatting.docx");
```

### Смотрите также

* class [ParagraphFormat](../../paragraphformat)
* пространство имен [Aspose.Words](../../paragraphformat)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->