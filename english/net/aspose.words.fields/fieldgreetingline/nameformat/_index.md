---
title: FieldGreetingLine.NameFormat
linktitle: NameFormat
articleTitle: NameFormat
second_title: Aspose.Words for .NET
description: Discover the FieldGreetingLine NameFormat property to easily customize name formats in your fields, enhancing user experience and personalization.
type: docs
weight: 40
url: /net/aspose.words.fields/fieldgreetingline/nameformat/
---
## FieldGreetingLine.NameFormat property

Gets or sets the format of the name included in the field.

```csharp
public string NameFormat { get; set; }
```

## Examples

Shows how to insert a GREETINGLINE field.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Create a generic greeting using a GREETINGLINE field, and some text after it.
FieldGreetingLine field = (FieldGreetingLine)builder.InsertField(FieldType.FieldGreetingLine, true);
builder.Writeln("\n\n\tThis is your custom greeting, created programmatically using Aspose Words!");

// A GREETINGLINE field accepts values from a data source during a mail merge, like a MERGEFIELD.
// It can also format how the source's data is written in its place once the mail merge is complete.
// The field names collection corresponds to the columns from the data source
// that the field will take values from.
Assert.That(field.GetFieldNames().Length, Is.EqualTo(0));

// To populate that array, we need to specify a format for our greeting line.
field.NameFormat = "<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> ";

// Now, our field will accept values from these two columns in the data source.
Assert.That(field.GetFieldNames()[0], Is.EqualTo("Courtesy Title"));
Assert.That(field.GetFieldNames()[1], Is.EqualTo("Last Name"));
Assert.That(field.GetFieldNames().Length, Is.EqualTo(2));

// This string will cover any cases where the data table data is invalid
// by substituting the malformed name with a string.
field.AlternateText = "Sir or Madam";

// Set a locale to format the result.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.That(field.GetFieldCode(), Is.EqualTo(" GREETINGLINE  \\f \"<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> \" \\e \"Sir or Madam\" \\l 1033"));

// Create a data table with columns whose names match elements
// from the field's field names collection, and then carry out the mail merge.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// This row has an invalid value in the Courtesy Title column, so our greeting will default to the alternate text.
table.Rows.Add("", "No", "Name");

doc.MailMerge.Execute(table);

Assert.That(doc.Range.Fields.Count, Is.EqualTo(0));
Assert.That(doc.GetText().Trim(), Is.EqualTo("Dear Mr. Doe,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Mrs. Cardholder,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Sir or Madam,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!"));
```

### See Also

* class [FieldGreetingLine](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
