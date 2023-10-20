---
title: HtmlLoadOptions.PreferredControlType
linktitle: PreferredControlType
articleTitle: PreferredControlType
second_title: Aspose.Words для .NET
description: HtmlLoadOptions PreferredControlType свойство. Получает или задает предпочтительный тип узлов документа которые будут представлять импортированные элементы input и select. Значение по умолчаниюFormField  на С#.
type: docs
weight: 50
url: /ru/net/aspose.words.loading/htmlloadoptions/preferredcontroltype/
---
## HtmlLoadOptions.PreferredControlType property

Получает или задает предпочтительный тип узлов документа, которые будут представлять импортированные элементы &lt;input&gt; и &lt;select&gt;. Значение по умолчанию:FormField .

```csharp
public HtmlControlType PreferredControlType { get; set; }
```

## Примечания

Обратите внимание, что установка этого свойства не гарантирует, что все импортированные элементы управления будут иметь указанный тип. Если элемент управления HTML не может быть представлен узлами документа предпочтительного типа, Aspose.Words будет использовать совместимый[`HtmlControlType`](../../htmlcontroltype/) для этого элемента управления.

## Примеры

Показывает, как установить предпочтительный тип узлов документа, которые будут представлять импортированные элементы &lt;input&gt; и &lt;select&gt;.

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

* enum [HtmlControlType](../../htmlcontroltype/)
* class [HtmlLoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
