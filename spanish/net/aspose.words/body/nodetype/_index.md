---
title: Body.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words para .NET
description: Descubra la propiedad Body NodeType que devuelve eficientemente el contenido del cuerpo, mejorando su experiencia de desarrollo web y agilizando sus proyectos.
type: docs
weight: 20
url: /es/net/aspose.words/body/nodetype/
---
## Body.NodeType property

DevuelveBody .

```csharp
public override NodeType NodeType { get; }
```

## Ejemplos

Muestra cómo iterar a través de los hijos de un nodo compuesto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Primary header");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("Primary footer");

Section section = doc.FirstSection;

// Una sección es un nodo compuesto y puede contener nodos secundarios,
// pero sólo si esos nodos secundarios son de un tipo de nodo "Body" o "HeaderFooter".
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

### Ver también

* enum [NodeType](../../nodetype/)
* class [Body](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
