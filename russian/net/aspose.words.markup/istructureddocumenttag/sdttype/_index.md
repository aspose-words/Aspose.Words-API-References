---
title: IStructuredDocumentTag.SdtType
linktitle: SdtType
articleTitle: SdtType
second_title: Aspose.Words для .NET
description: Откройте для себя свойство IStructuredDocumentTag SdtType, чтобы легко определить тип структурированных тегов документа для улучшенного управления документами.
type: docs
weight: 120
url: /ru/net/aspose.words.markup/istructureddocumenttag/sdttype/
---
## IStructuredDocumentTag.SdtType property

Получает тип этого**Структурированный тег документа** .

```csharp
public SdtType SdtType { get; }
```

## Примеры

Показывает, как получить тип тега структурированного документа.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

List<StructuredDocumentTag> tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true)
    .OfType<StructuredDocumentTag>().ToList();

Assert.AreEqual(SdtType.RepeatingSection, tags[0].SdtType);
Assert.AreEqual(SdtType.RepeatingSectionItem, tags[1].SdtType);
Assert.AreEqual(SdtType.RichText, tags[2].SdtType);
```

### Смотрите также

* enum [SdtType](../../sdttype/)
* interface [IStructuredDocumentTag](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
