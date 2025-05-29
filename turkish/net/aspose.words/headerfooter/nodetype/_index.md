---
title: HeaderFooter.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: .NET için Aspose.Words
description: İçerik yapınızı ve kullanıcı deneyiminizi geliştirerek başlık ve altbilgi ayrıntılarını etkili bir şekilde alan HeaderFooter NodeType özelliğini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words/headerfooter/nodetype/
---
## HeaderFooter.NodeType property

Geri DöndürürHeaderFooter .

```csharp
public override NodeType NodeType { get; }
```

## Örnekler

Bir bileşik düğümün alt düğümleri arasında nasıl yineleme yapılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Primary header");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("Primary footer");

Section section = doc.FirstSection;

// Bir Bölüm, bileşik bir düğümdür ve alt düğümler içerebilir,
// ancak yalnızca bu alt düğümler "Body" veya "HeaderFooter" düğüm türündeyse.
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

### Ayrıca bakınız

* enum [NodeType](../../nodetype/)
* class [HeaderFooter](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
