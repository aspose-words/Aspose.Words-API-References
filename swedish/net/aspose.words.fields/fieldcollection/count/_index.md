---
title: FieldCollection.Count
second_title: Aspose.Words för .NET API Referens
description: FieldCollection fast egendom. Returnerar antalet fält i samlingen.
type: docs
weight: 10
url: /sv/net/aspose.words.fields/fieldcollection/count/
---
## FieldCollection.Count property

Returnerar antalet fält i samlingen.

```csharp
public int Count { get; }
```

### Exempel

Visar hur man tar bort fält från en fältsamling.

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

// Nedan finns fyra sätt att ta bort fält från en fältsamling.
// 1 - Få ett fält för att ta bort sig själv:
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - Få samlingen för att ta bort ett fält som vi skickar till dess borttagningsmetod:
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 - Ta bort ett fält från en samling vid ett index:
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 - Ta bort alla fält från samlingen på en gång:
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

Visar hur man arbetar med en samling fält.

```csharp
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

    // Iterera över fältsamlingen och skriv ut innehåll och skriv
    // av varje fält med en anpassad besöksimplementering.
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

/// <summary>
/// Dokumentbesökarimplementering som skriver ut fältinformation.
/// </summary>
public class FieldVisitor : DocumentVisitor
{
    public FieldVisitor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Hämtar vanlig text av dokumentet som samlades av besökaren.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Anropas när en FieldStart-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        mBuilder.AppendLine("Found field: " + fieldStart.FieldType);
        mBuilder.AppendLine("\tField code: " + fieldStart.GetField().GetFieldCode());
        mBuilder.AppendLine("\tDisplayed as: " + fieldStart.GetField().Result);

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en FieldSeparator-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        mBuilder.AppendLine("\tFound separator: " + fieldSeparator.GetText());

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en FieldEnd-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mBuilder.AppendLine("End of field: " + fieldEnd.FieldType);

        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
}
```

### Se även

* class [FieldCollection](../)
* namnutrymme [Aspose.Words.Fields](../../fieldcollection/)
* hopsättning [Aspose.Words](../../../)


