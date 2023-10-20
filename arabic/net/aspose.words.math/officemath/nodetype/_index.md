---
title: OfficeMath.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words لـ .NET
description: OfficeMath NodeType ملكية. إرجاعOfficeMath  في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.math/officemath/nodetype/
---
## OfficeMath.NodeType property

إرجاعOfficeMath .

```csharp
public override NodeType NodeType { get; }
```

## أمثلة

يوضح كيفية ضبط تنسيق عرض الرياضيات المكتبية.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

// عقد OfficeMath التابعة لعقد OfficeMath الأخرى تكون دائمًا مضمّنة.
// العقدة التي نعمل معها هي العقدة الأساسية لتغيير موقعها ونوع العرض.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// تغيير الموقع ونوع العرض لعقدة OfficeMath.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### أنظر أيضا

* enum [NodeType](../../../aspose.words/nodetype/)
* class [OfficeMath](../)
* مساحة الاسم [Aspose.Words.Math](../../../aspose.words.math/)
* المجسم [Aspose.Words](../../../)
