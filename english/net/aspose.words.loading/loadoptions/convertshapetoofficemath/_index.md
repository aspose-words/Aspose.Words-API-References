---
title: LoadOptions.ConvertShapeToOfficeMath
linktitle: ConvertShapeToOfficeMath
articleTitle: ConvertShapeToOfficeMath
second_title: Aspose.Words for .NET
description: Transform shapes with EquationXML into Office Math objects effortlessly using LoadOptions' ConvertShapeToOfficeMath property for enhanced document clarity.
type: docs
weight: 40
url: /net/aspose.words.loading/loadoptions/convertshapetoofficemath/
---
## LoadOptions.ConvertShapeToOfficeMath property

Gets or sets whether to convert shapes with EquationXML to Office Math objects.

```csharp
public bool ConvertShapeToOfficeMath { get; set; }
```

## Examples

Shows how to convert EquationXML shapes to Office Math objects.

```csharp
LoadOptions loadOptions = new LoadOptions();

// Use this flag to specify whether to convert the shapes with EquationXML attributes
// to Office Math objects and then load the document.
loadOptions.ConvertShapeToOfficeMath = isConvertShapeToOfficeMath;

Document doc = new Document(MyDir + "Math shapes.docx", loadOptions);

if (isConvertShapeToOfficeMath)
{
    Assert.AreEqual(16, doc.GetChildNodes(NodeType.Shape, true).Count);
    Assert.AreEqual(34, doc.GetChildNodes(NodeType.OfficeMath, true).Count);
}
else
{
    Assert.AreEqual(24, doc.GetChildNodes(NodeType.Shape, true).Count);
    Assert.AreEqual(0, doc.GetChildNodes(NodeType.OfficeMath, true).Count);
}
```

### See Also

* class [LoadOptions](../)
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
