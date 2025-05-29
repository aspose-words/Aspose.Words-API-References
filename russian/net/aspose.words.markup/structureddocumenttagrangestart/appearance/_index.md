---
title: StructuredDocumentTagRangeStart.Appearance
linktitle: Appearance
articleTitle: Appearance
second_title: Aspose.Words для .NET
description: Узнайте, как настроить внешний вид StructuredDocumentTagRangeStart для улучшенного форматирования документа и повышения его читабельности.
type: docs
weight: 20
url: /ru/net/aspose.words.markup/structureddocumenttagrangestart/appearance/
---
## StructuredDocumentTagRangeStart.Appearance property

Возвращает или задает внешний вид структурированного тега документа.

```csharp
public SdtAppearance Appearance { get; set; }
```

## Примеры

Показывает, как отображать теги вокруг контента.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");
StructuredDocumentTagRangeStart tag =
    doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true) as StructuredDocumentTagRangeStart;

if (tag.Appearance == SdtAppearance.Hidden)
    tag.Appearance = SdtAppearance.Tags;
```

### Смотрите также

* enum [SdtAppearance](../../sdtappearance/)
* class [StructuredDocumentTagRangeStart](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
