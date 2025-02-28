---
title: OleFormat.SuggestedFileName
linktitle: SuggestedFileName
articleTitle: SuggestedFileName
second_title: Aspose.Words for .NET
description: Discover the OleFormat SuggestedFileName property to easily retrieve the recommended file name for saving your embedded objects seamlessly.
type: docs
weight: 130
url: /net/aspose.words.drawing/oleformat/suggestedfilename/
---
## OleFormat.SuggestedFileName property

Gets the file name suggested for the current embedded object if you want to save it into a file.

```csharp
public string SuggestedFileName { get; }
```

## Examples

Shows how to get an OLE object's suggested file name.

```csharp
Document doc = new Document(MyDir + "OLE shape.rtf");

Shape oleShape = (Shape)doc.FirstSection.Body.GetChild(NodeType.Shape, 0, true);

// OLE objects can provide a suggested filename and extension,
// which we can use when saving the object's contents into a file in the local file system.
string suggestedFileName = oleShape.OleFormat.SuggestedFileName;

Assert.AreEqual("CSV.csv", suggestedFileName);

using (FileStream fileStream = new FileStream(ArtifactsDir + suggestedFileName, FileMode.Create))
{
    oleShape.OleFormat.Save(fileStream);
}
```

### See Also

* class [OleFormat](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
