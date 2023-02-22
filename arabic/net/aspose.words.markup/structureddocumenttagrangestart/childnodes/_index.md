---
title: StructuredDocumentTagRangeStart.ChildNodes
second_title: Aspose.Words لمراجع .NET API
description: StructuredDocumentTagRangeStart ملكية. يحصل على جميع العقد بين عقدة بداية النطاق وعقدة نهاية النطاق.
type: docs
weight: 20
url: /ar/net/aspose.words.markup/structureddocumenttagrangestart/childnodes/
---
## StructuredDocumentTagRangeStart.ChildNodes property

يحصل على جميع العقد بين عقدة بداية النطاق وعقدة نهاية النطاق.

```csharp
public NodeCollection ChildNodes { get; }
```

### أمثلة

يوضح كيفية الحصول على العقد الفرعية لـ StructuredDocumentTagRangeStart.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");
StructuredDocumentTagRangeStart tag =
    doc.GetChildNodes(NodeType.StructuredDocumentTagRangeStart, true)[0] as StructuredDocumentTagRangeStart;

Console.WriteLine("StructuredDocumentTagRangeStart values:");
Console.WriteLine($"\t|Child nodes count: {tag.ChildNodes.Count}\n");

foreach (Node node in tag.ChildNodes)
    Console.WriteLine($"\t|Child node type: {node.NodeType}");

foreach (Node node in tag.GetChildNodes(NodeType.Run, true))
    Console.WriteLine($"\t|Child node text: {node.GetText()}");
```

### أنظر أيضا

* class [NodeCollection](../../../aspose.words/nodecollection/)
* class [StructuredDocumentTagRangeStart](../)
* مساحة الاسم [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* المجسم [Aspose.Words](../../../)


