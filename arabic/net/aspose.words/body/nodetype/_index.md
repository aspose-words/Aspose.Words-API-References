---
title: Body.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Body NodeType التي تقوم بإرجاع محتوى النص بكفاءة، مما يعمل على تحسين تجربة تطوير الويب لديك وتبسيط مشاريعك.
type: docs
weight: 20
url: /ar/net/aspose.words/body/nodetype/
---
## Body.NodeType property

إرجاعBody .

```csharp
public override NodeType NodeType { get; }
```

## أمثلة

يوضح كيفية التكرار خلال أبناء العقدة المركبة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Primary header");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("Primary footer");

Section section = doc.FirstSection;

// القسم عبارة عن عقدة مركبة ويمكن أن تحتوي على عقد فرعية،
// ولكن فقط إذا كانت هذه العقد الفرعية من نوع عقدة "Body" أو "HeaderFooter".
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

### أنظر أيضا

* enum [NodeType](../../nodetype/)
* class [Body](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
