---
title: ParagraphFormat.LeftIndent
second_title: Справочник по API Aspose.Words для .NET
description: ParagraphFormat свойство. Получает или задает значение в пунктах представляющее левый отступ абзаца.
type: docs
weight: 180
url: /ru/net/aspose.words/paragraphformat/leftindent/
---
## ParagraphFormat.LeftIndent property

Получает или задает значение (в пунктах), представляющее левый отступ абзаца.

```csharp
public double LeftIndent { get; set; }
```

### Примеры

Показывает, как настроить форматирование абзаца для создания текста со смещением от центра.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Центрируем весь текст, который пишет конструктор документов, и устанавливаем отступы.
// Приведенная ниже конфигурация отступа создаст текст, который будет асимметрично располагаться на странице.
// «Центром», по которому мы выравниваем текст, будет середина текста, а не середина страницы.
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

* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../paragraphformat/)
* сборка [Aspose.Words](../../../)


