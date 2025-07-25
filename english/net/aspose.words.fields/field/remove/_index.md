---
title: Field.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words for .NET
description: Effortlessly remove fields from documents with the Field Remove method. Get precise node returns and handle empty fields seamlessly. Optimize your workflow!
type: docs
weight: 120
url: /net/aspose.words.fields/field/remove/
---
## Field.Remove method

Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns `null`.

```csharp
public Node Remove()
```

## Examples

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

Assert.That(fields.Count, Is.EqualTo(6));

// Below are four ways of removing fields from a field collection.
// 1 -  Get a field to remove itself:
fields[0].Remove();
Assert.That(fields.Count, Is.EqualTo(5));

// 2 -  Get the collection to remove a field that we pass to its removal method:
Field lastField = fields[3];
fields.Remove(lastField);
Assert.That(fields.Count, Is.EqualTo(4));

// 3 -  Remove a field from a collection at an index:
fields.RemoveAt(2);
Assert.That(fields.Count, Is.EqualTo(3));

// 4 -  Remove all the fields from the collection at once:
fields.Clear();
Assert.That(fields.Count, Is.EqualTo(0));
```

Shows how to process PRIVATE fields.

```csharp
public void FieldPrivate()
{
    // Open a Corel WordPerfect document which we have converted to .docx format.
    Document doc = new Document(MyDir + "Field sample - PRIVATE.docx");

    // WordPerfect 5.x/6.x documents like the one we have loaded may contain PRIVATE fields.
    // Microsoft Word preserves PRIVATE fields during load/save operations,
    // but provides no functionality for them.
    FieldPrivate field = (FieldPrivate)doc.Range.Fields[0];

    Assert.That(field.GetFieldCode(), Is.EqualTo(" PRIVATE \"My value\" "));
    Assert.That(field.Type, Is.EqualTo(FieldType.FieldPrivate));

    // We can also insert PRIVATE fields using a document builder.
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(FieldType.FieldPrivate, true);

    // These fields are not a viable way of protecting sensitive information.
    // Unless backward compatibility with older versions of WordPerfect is essential,
    // we can safely remove these fields. We can do this using a DocumentVisiitor implementation.
    Assert.That(doc.Range.Fields.Count, Is.EqualTo(2));

    FieldPrivateRemover remover = new FieldPrivateRemover();
    doc.Accept(remover);

    Assert.That(remover.GetFieldsRemovedCount(), Is.EqualTo(2));
    Assert.That(doc.Range.Fields.Count, Is.EqualTo(0));
}

/// <summary>
/// Removes all encountered PRIVATE fields.
/// </summary>
public class FieldPrivateRemover : DocumentVisitor
{
    public FieldPrivateRemover()
    {
        mFieldsRemovedCount = 0;
    }

    public int GetFieldsRemovedCount()
    {
        return mFieldsRemovedCount;
    }

    /// <summary>
    /// Called when a FieldEnd node is encountered in the document.
    /// If the node belongs to a PRIVATE field, the entire field is removed.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        if (fieldEnd.FieldType == FieldType.FieldPrivate)
        {
            fieldEnd.GetField().Remove();
            mFieldsRemovedCount++;
        }

        return VisitorAction.Continue;
    }

    private int mFieldsRemovedCount;
}
```

### See Also

* class [Node](../../../aspose.words/node/)
* class [Field](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
