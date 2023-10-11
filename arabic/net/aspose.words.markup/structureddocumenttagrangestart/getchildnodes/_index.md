---
title: StructuredDocumentTagRangeStart.GetChildNodes
second_title: Aspose.Words لمراجع .NET API
description: StructuredDocumentTagRangeStart طريقة. إرجاع مجموعة مباشرة من العقد الفرعية التي تطابق الأنواع المحددة.
type: docs
weight: 210
url: /ar/net/aspose.words.markup/structureddocumenttagrangestart/getchildnodes/
---
## StructuredDocumentTagRangeStart.GetChildNodes method

إرجاع مجموعة مباشرة من العقد الفرعية التي تطابق الأنواع المحددة.

```csharp
public NodeCollection GetChildNodes(NodeType nodeType, bool isDeep)
```

### أمثلة

يوضح كيفية الحصول على العقد الفرعية لـ StructuredDocumentTagRangeStart.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");
StructuredDocumentTagRangeStart tag =
    doc.GetChildNodes(NodeType.StructuredDocumentTagRangeStart, true)[0] as StructuredDocumentTagRangeStart;

Console.WriteLine("StructuredDocumentTagRangeStart values:");
Console.WriteLine($"\t|Child nodes count: {tag.GetChildNodes(NodeType.Any, false).Count}\n");

foreach (Node node in tag.GetChildNodes(NodeType.Any, false))
    Console.WriteLine($"\t|Child node type: {node.NodeType}");

foreach (Node node in tag.GetChildNodes(NodeType.Run, true))
    Console.WriteLine($"\t|Child node text: {node.GetText()}");
```

### أنظر أيضا

* class [NodeCollection](../../../aspose.words/nodecollection/)
* enum [NodeType](../../../aspose.words/nodetype/)
* class [StructuredDocumentTagRangeStart](../)
* مساحة الاسم [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* المجسم [Aspose.Words](../../../)


