---
title: SdtAppearance Enum
linktitle: SdtAppearance
articleTitle: SdtAppearance
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Markup.SdtAppearance для настройки внешнего вида структурированных тегов документов. Улучшите форматирование документов без усилий!
type: docs
weight: 4680
url: /ru/net/aspose.words.markup/sdtappearance/
---
## SdtAppearance enumeration

Задает внешний вид структурированного тега документа.

```csharp
public enum SdtAppearance
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| BoundingBox | `0` | Представляет структурированный тег документа, отображаемый в виде затененного прямоугольника или ограничивающей рамки. |
| Tags | `1` | Представляет структурированный тег документа, отображаемый как начальный и конечный маркеры. |
| Hidden | `2` | Представляет структурированный тег документа, который не отображается. |
| Default | `0` | По умолчаниюBoundingBox . |

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

* пространство имен [Aspose.Words.Markup](../../aspose.words.markup/)
* сборка [Aspose.Words](../../)
