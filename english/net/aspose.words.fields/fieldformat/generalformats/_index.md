---
title: FieldFormat.GeneralFormats
linktitle: GeneralFormats
articleTitle: GeneralFormats
second_title: Aspose.Words for .NET
description: Discover the FieldFormat GeneralFormats property, offering a versatile collection of numeric text formats to enhance your data presentation and results.
type: docs
weight: 20
url: /net/aspose.words.fields/fieldformat/generalformats/
---
## FieldFormat.GeneralFormats property

Gets a collection of general formats that are applied to a numeric, text or any field result. Corresponds to the \* switches.

```csharp
public GeneralFormatCollection GeneralFormats { get; }
```

## Examples

Shows how to format field results.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Use a document builder to insert a field that displays a result with no format applied.
Field field = builder.InsertField("= 2 + 3");

Assert.That(field.GetFieldCode(), Is.EqualTo("= 2 + 3"));
Assert.That(field.Result, Is.EqualTo("5"));

// We can apply a format to a field's result using the field's properties.
// Below are three types of formats that we can apply to a field's result.
// 1 -  Numeric format:
FieldFormat format = field.Format;
format.NumericFormat = "$###.00";
field.Update();

Assert.That(field.GetFieldCode(), Is.EqualTo("= 2 + 3 \\# $###.00"));
Assert.That(field.Result, Is.EqualTo("$  5.00"));

// 2 -  Date/time format:
field = builder.InsertField("DATE");
format = field.Format;
format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

Assert.That(field.GetFieldCode(), Is.EqualTo("DATE \\@ \"dddd, MMMM dd, yyyy\""));
Console.WriteLine($"Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

// 3 -  General format:
field = builder.InsertField("= 25 + 33");
format = field.Format;
format.GeneralFormats.Add(GeneralFormat.LowercaseRoman);
format.GeneralFormats.Add(GeneralFormat.Upper);
field.Update();

int index = 0;
using (IEnumerator<GeneralFormat> generalFormatEnumerator = format.GeneralFormats.GetEnumerator())
    while (generalFormatEnumerator.MoveNext())
        Console.WriteLine($"General format index {index++}: {generalFormatEnumerator.Current}");

Assert.That(field.GetFieldCode(), Is.EqualTo("= 25 + 33 \\* roman \\* Upper"));
Assert.That(field.Result, Is.EqualTo("LVIII"));
Assert.That(format.GeneralFormats.Count, Is.EqualTo(2));
Assert.That(format.GeneralFormats[0], Is.EqualTo(GeneralFormat.LowercaseRoman));

// We can remove our formats to revert the field's result to its original form.
format.GeneralFormats.Remove(GeneralFormat.LowercaseRoman);
format.GeneralFormats.RemoveAt(0);
Assert.That(format.GeneralFormats.Count, Is.EqualTo(0));
field.Update();

Assert.That(field.GetFieldCode(), Is.EqualTo("= 25 + 33  "));
Assert.That(field.Result, Is.EqualTo("58"));
Assert.That(format.GeneralFormats.Count, Is.EqualTo(0));
```

### See Also

* class [GeneralFormatCollection](../../generalformatcollection/)
* class [FieldFormat](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
