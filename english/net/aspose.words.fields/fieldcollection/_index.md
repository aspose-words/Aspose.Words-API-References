---
title: FieldCollection
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 1510
url: /net/aspose.words.fields/fieldcollection/
---
## FieldCollection class

A collection of [`Field`](../field) objects that represents the fields in the specified range.

```csharp
public class FieldCollection : IEnumerable<Field>
```

## Public Members

| Name | Description |
| --- | --- |
| [Count](count) { get; } | Returns the number of the fields in the collection. |
| [Item](item) { get; } | Returns a field at the specified index. |
| [Clear](clear)() | Removes all fields of this collection from the document and from this collection itself. |
| [GetEnumerator](getenumerator)() | Returns an enumerator object. |
| [Remove](remove)(…) | Removes the specified field from this collection and from the document. |
| [RemoveAt](removeat)(…) | Removes a field at the specified index from this collection and from the document. |

### Remarks

An instance of this collection iterates fields which start fall within the specified range.The [`FieldCollection`](../fieldcollection) collection does not own the fields it contains, rather, is just a selection of fields.The [`FieldCollection`](../fieldcollection) collection is "live", i.e. changes to the children of the node object that it was created from are immediately reflected in the fields returned by the [`FieldCollection`](../fieldcollection) properties and methods.

### Examples

Shows how to remove fields from a field collection.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
builder.InsertField(" TIME ");
builder.InsertField(" REVNUM ");
builder.InsertField(" AUTHOR  \"John Doe\" ");
builder.InsertField(" SUBJECT \"My Subject\" ");
builder.InsertField(" QUOTE \"Hello world!\" ");
doc.UpdateFields();

FieldCollection fields = doc.Range.Fields;

Assert.AreEqual(6, fields.Count);

// Below are four ways of removing fields from a field collection.
// 1 -  Get a field to remove itself:
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 -  Get the collection to remove a field that we pass to its removal method:
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 -  Remove a field from a collection at an index:
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 -  Remove all the fields from the collection at once:
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

Shows how to work with a collection of fields.

```csharp
public void FieldCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
    builder.InsertField(" TIME ");
    builder.InsertField(" REVNUM ");
    builder.InsertField(" AUTHOR  \"John Doe\" ");
    builder.InsertField(" SUBJECT \"My Subject\" ");
    builder.InsertField(" QUOTE \"Hello world!\" ");
    doc.UpdateFields();

    FieldCollection fields = doc.Range.Fields;

    Assert.AreEqual(6, fields.Count);

    // Iterate over the field collection, and print contents and type
    // of every field using a custom visitor implementation.
    FieldVisitor fieldVisitor = new FieldVisitor();

    using (IEnumerator<Field> fieldEnumerator = fields.GetEnumerator())
    {
        while (fieldEnumerator.MoveNext())
        {
            if (fieldEnumerator.Current != null)
            {
                fieldEnumerator.Current.Start.Accept(fieldVisitor);
                fieldEnumerator.Current.Separator?.Accept(fieldVisitor);
                fieldEnumerator.Current.End.Accept(fieldVisitor);
            }
            else
            {
                Console.WriteLine("There are no fields in the document.");
            }
        }
    }

    Console.WriteLine(fieldVisitor.GetText());
}

/// <summary>
/// Document visitor implementation that prints field info.
/// </summary>
public class FieldVisitor : DocumentVisitor
{
    public FieldVisitor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Gets the plain text of the document that was accumulated by the visitor.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Called when a FieldStart node is encountered in the document.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        mBuilder.AppendLine("Found field: " + fieldStart.FieldType);
        mBuilder.AppendLine("\tField code: " + fieldStart.GetField().GetFieldCode());
        mBuilder.AppendLine("\tDisplayed as: " + fieldStart.GetField().Result);

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Called when a FieldSeparator node is encountered in the document.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        mBuilder.AppendLine("\tFound separator: " + fieldSeparator.GetText());

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Called when a FieldEnd node is encountered in the document.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mBuilder.AppendLine("End of field: " + fieldEnd.FieldType);

        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
}
```

### See Also

* class [Field](../field)
* namespace [Aspose.Words.Fields](../../aspose.words.fields)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
