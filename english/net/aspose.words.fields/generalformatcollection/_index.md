---
title: GeneralFormatCollection Class
linktitle: GeneralFormatCollection
articleTitle: GeneralFormatCollection
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Fields.GeneralFormatCollection class—a powerful, typed collection for managing general formats effortlessly in your documents.
type: docs
weight: 3060
url: /net/aspose.words.fields/generalformatcollection/
---
## GeneralFormatCollection class

Represents a typed collection of general formats.

To learn more, visit the [Working with Fields](https://docs.aspose.com/words/net/working-with-fields/) documentation article.

```csharp
public class GeneralFormatCollection : IEnumerable<GeneralFormat>
```

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words.fields/generalformatcollection/count/) { get; } | Gets the total number of the items in the collection. |
| [Item](../../aspose.words.fields/generalformatcollection/item/) { get; } | Gets a general format at the specified index. |

## Methods

| Name | Description |
| --- | --- |
| [Add](../../aspose.words.fields/generalformatcollection/add/)(*[GeneralFormat](../generalformat/)*) | Adds a general format to the collection. |
| [GetEnumerator](../../aspose.words.fields/generalformatcollection/getenumerator/)() | Returns an enumerator object. |
| [Remove](../../aspose.words.fields/generalformatcollection/remove/)(*[GeneralFormat](../generalformat/)*) | Removes all occurrences of the specified general format from the collection. |
| [RemoveAt](../../aspose.words.fields/generalformatcollection/removeat/)(*int*) | Removes a general format occurrence at the specified index. |

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

* enum [GeneralFormat](../generalformat/)
* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)
