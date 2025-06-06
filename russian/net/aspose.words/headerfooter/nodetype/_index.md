---
title: HeaderFooter.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words для .NET
description: Откройте для себя свойство HeaderFooter NodeType, которое эффективно извлекает данные верхнего и нижнего колонтитула, улучшая структуру контента и пользовательский опыт.
type: docs
weight: 50
url: /ru/net/aspose.words/headerfooter/nodetype/
---
## HeaderFooter.NodeType property

ВозвратHeaderFooter .

```csharp
public override NodeType NodeType { get; }
```

## Примеры

Показывает, как перебирать дочерние элементы составного узла.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Primary header");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("Primary footer");

Section section = doc.FirstSection;

// Раздел — это составной узел, который может содержать дочерние узлы,
// но только если эти дочерние узлы имеют тип узла "Body" или "HeaderFooter".
foreach (Node node in section)
{
    switch (node.NodeType)
    {
        case NodeType.Body:
        {
            Body body = (Body)node;

            Console.WriteLine("Body:");
            Console.WriteLine($"\t\"{body.GetText().Trim()}\"");
            break;
        }
        case NodeType.HeaderFooter:
        {
            HeaderFooter headerFooter = (HeaderFooter)node;

            Console.WriteLine($"HeaderFooter type: {headerFooter.HeaderFooterType}:");
            Console.WriteLine($"\t\"{headerFooter.GetText().Trim()}\"");
            break;
        }
        default:
        {
            throw new Exception("Unexpected node type in a section.");
        }
    }
}
```

### Смотрите также

* enum [NodeType](../../nodetype/)
* class [HeaderFooter](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
