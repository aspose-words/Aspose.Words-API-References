---
title: Body.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Body NodeType qui renvoie efficacement le contenu du corps, améliorant ainsi votre expérience de développement Web et rationalisant vos projets.
type: docs
weight: 20
url: /fr/net/aspose.words/body/nodetype/
---
## Body.NodeType property

RetoursBody .

```csharp
public override NodeType NodeType { get; }
```

## Exemples

Montre comment parcourir les enfants d'un nœud composite.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Primary header");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("Primary footer");

Section section = doc.FirstSection;

// Une section est un nœud composite et peut contenir des nœuds enfants,
// mais seulement si ces nœuds enfants sont de type nœud « Body » ou « HeaderFooter ».
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

### Voir également

* enum [NodeType](../../nodetype/)
* class [Body](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
