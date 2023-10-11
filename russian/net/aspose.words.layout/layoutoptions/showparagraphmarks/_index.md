---
title: LayoutOptions.ShowParagraphMarks
second_title: Справочник по API Aspose.Words для .NET
description: LayoutOptions свойство. Получает или задает индикатор того отображаются ли знаки абзаца. Значение по умолчаниюЛОЖЬ .
type: docs
weight: 90
url: /ru/net/aspose.words.layout/layoutoptions/showparagraphmarks/
---
## LayoutOptions.ShowParagraphMarks property

Получает или задает индикатор того, отображаются ли знаки абзаца. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ShowParagraphMarks { get; set; }
```

### Примеры

Показывает, как отображать знаки абзаца в готовом к просмотру выходном документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Добавляем несколько абзацев, затем включаем знаки абзацев, чтобы показывать концы абзацев
// с символом подставки (¶) при рендеринге документа.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

### Смотрите также

* class [LayoutOptions](../)
* пространство имен [Aspose.Words.Layout](../../layoutoptions/)
* сборка [Aspose.Words](../../../)


