---
title: IStructuredDocumentTag.Appearance
linktitle: Appearance
articleTitle: Appearance
second_title: Aspose.Words для .NET
description: Откройте для себя свойство IStructuredDocumentTag Appearance, чтобы настраивать и улучшать структурированные теги документов для улучшения пользовательского опыта.
type: docs
weight: 10
url: /ru/net/aspose.words.markup/istructureddocumenttag/appearance/
---
## IStructuredDocumentTag.Appearance property

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
* interface [IStructuredDocumentTag](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
