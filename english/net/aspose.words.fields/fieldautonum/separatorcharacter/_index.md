---
title: FieldAutoNum.SeparatorCharacter
linktitle: SeparatorCharacter
articleTitle: SeparatorCharacter
second_title: Aspose.Words for .NET
description: Discover the FieldAutoNum SeparatorCharacter property, easily customize your separator character for enhanced data formatting and improved usability.
type: docs
weight: 20
url: /net/aspose.words.fields/fieldautonum/separatorcharacter/
---
## FieldAutoNum.SeparatorCharacter property

Gets or sets the separator character to be used.

```csharp
public string SeparatorCharacter { get; set; }
```

## Examples

Shows how to number paragraphs using autonum fields.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Each AUTONUM field displays the current value of a running count of AUTONUM fields,
// allowing us to automatically number items like a numbered list.
// This field will display a number "1.".
FieldAutoNum field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 1.");

Assert.AreEqual(" AUTONUM ", field.GetFieldCode());

field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 2.");

// The separator character, which appears in the field result immediately after the number,is a full stop by default.
// If we leave this property null, our second AUTONUM field will display "2." in the document.
Assert.IsNull(field.SeparatorCharacter);

// We can set this property to apply the first character of its string as the new separator character.
// In this case, our AUTONUM field will now display "2:".
field.SeparatorCharacter = ":";

Assert.AreEqual(" AUTONUM  \\s :", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.AUTONUM.docx");
```

### See Also

* class [FieldAutoNum](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
