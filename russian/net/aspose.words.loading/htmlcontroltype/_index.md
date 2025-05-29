---
title: HtmlControlType Enum
linktitle: HtmlControlType
articleTitle: HtmlControlType
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.HtmlControlType для бесшовного импорта входных данных HTML и выбора элементов, расширяя возможности обработки документов.
type: docs
weight: 4060
url: /ru/net/aspose.words.loading/htmlcontroltype/
---
## HtmlControlType enumeration

Тип узлов документа, представляющих элементы &lt;input&gt; и &lt;select&gt;, импортированные из HTML.

```csharp
public enum HtmlControlType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| FormField | `0` | Поле формы. |
| StructuredDocumentTag | `1` | Структурированный тег документа |

## Примеры

Показывает, как задать предпочтительный тип узлов документа, которые будут представлять импортированные элементы &lt;input&gt; и &lt;select&gt;.

```csharp
const string html = @"
    <html>
        <select name='ComboBox' size='1'>
            <option value='val1'>item1</option>
            <option value='val2'></option>
        </select>
    </html>
";

HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions();
htmlLoadOptions.PreferredControlType = HtmlControlType.StructuredDocumentTag;

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), htmlLoadOptions);
NodeCollection nodes = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

StructuredDocumentTag tag = (StructuredDocumentTag) nodes[0];
```

### Смотрите также

* пространство имен [Aspose.Words.Loading](../../aspose.words.loading/)
* сборка [Aspose.Words](../../)
