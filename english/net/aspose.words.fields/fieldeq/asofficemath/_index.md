---
title: FieldEQ.AsOfficeMath
linktitle: AsOfficeMath
articleTitle: AsOfficeMath
second_title: Aspose.Words for .NET
description: FieldEQ AsOfficeMath method. Returns Office Math object corresponded to the EQ field in C#.
type: docs
weight: 20
url: /net/aspose.words.fields/fieldeq/asofficemath/
---
## FieldEQ.AsOfficeMath method

Returns Office Math object corresponded to the EQ field.

```csharp
public OfficeMath AsOfficeMath()
```

### Return Value

Returns `null` if field code is empty or invalid, otherwise an [`OfficeMath`](../../../aspose.words.math/officemath/) instance.

## Examples

Shows how to replace the EQ field with Office Math.

```csharp
Document doc = new Document(MyDir + "Field sample - EQ.docx");
FieldEQ fieldEQ = doc.Range.Fields.OfType<FieldEQ>().First();

OfficeMath officeMath = fieldEQ.AsOfficeMath();

fieldEQ.Start.ParentNode.InsertBefore(officeMath, fieldEQ.Start);
fieldEQ.Remove();

doc.Save(ArtifactsDir + "Field.EQAsOfficeMath.docx");
```

### See Also

* class [OfficeMath](../../../aspose.words.math/officemath/)
* class [FieldEQ](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
