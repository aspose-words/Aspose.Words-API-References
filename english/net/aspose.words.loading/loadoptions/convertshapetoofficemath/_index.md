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
    Assert.That(doc.GetChildNodes(NodeType.Shape, true).Count, Is.EqualTo(16));
    Assert.That(doc.GetChildNodes(NodeType.OfficeMath, true).Count, Is.EqualTo(34));
}
else
{
    Assert.That(doc.GetChildNodes(NodeType.Shape, true).Count, Is.EqualTo(24));
    Assert.That(doc.GetChildNodes(NodeType.OfficeMath, true).Count, Is.EqualTo(0));
}
```

### See Also

* class [LoadOptions](../)
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
