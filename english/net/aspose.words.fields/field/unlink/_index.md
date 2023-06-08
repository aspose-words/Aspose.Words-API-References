---
title: Field.Unlink
linktitle: Unlink
articleTitle: Unlink
second_title: Aspose.Words for .NET
description: Field Unlink method. Performs the field unlink in C#.
type: docs
weight: 130
url: /net/aspose.words.fields/field/unlink/
---
## Field.Unlink method

Performs the field unlink.

```csharp
public bool Unlink()
```

### Return Value

`true` if the field has been unlinked, otherwise `false`.

## Remarks

Replaces the field with its most recent result.

Some fields, such as XE (Index Entry) fields and SEQ (Sequence) fields, cannot be unlinked.

## Examples

Shows how to unlink a field.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");
doc.Range.Fields[1].Unlink();
```

### See Also

* class [Field](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
