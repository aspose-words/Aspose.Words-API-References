---
title: MailMerge.DeleteFields
linktitle: DeleteFields
articleTitle: DeleteFields
second_title: Aspose.Words for .NET
description: Effortlessly streamline your documents with the MailMerge DeleteFields method, removing unnecessary mail merge fields for cleaner, more professional results.
type: docs
weight: 170
url: /net/aspose.words.mailmerging/mailmerge/deletefields/
---
## MailMerge.DeleteFields method

Removes mail merge related fields from the document.

```csharp
public void DeleteFields()
```

## Remarks

This method removes MERGEFIELD and NEXT fields from the document.

This method could be useful if your mail merge operation does not always need to populate all fields in the document. Use this method to remove all remaining mail merge fields.

## Examples

Shows how to delete all MERGEFIELDs from a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.Writeln(",");
builder.Writeln("Greetings!");

Assert.That(doc.GetText().Trim(), Is.EqualTo("Dear \u0013 MERGEFIELD FirstName \u0014«FirstName»\u0015 \u0013 MERGEFIELD LastName \u0014«LastName»\u0015,\rGreetings!"));

doc.MailMerge.DeleteFields();

Assert.That(doc.GetText().Trim(), Is.EqualTo("Dear  ,\rGreetings!"));
```

### See Also

* class [MailMerge](../)
* namespace [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assembly [Aspose.Words](../../../)
