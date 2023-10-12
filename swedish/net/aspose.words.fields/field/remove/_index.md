---
title: Field.Remove
second_title: Aspose.Words för .NET API Referens
description: Field metod. Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista child av dess överordnade nod returnerar dess överordnade stycke. Om fältet redan är borttaget returnerasnull .
type: docs
weight: 120
url: /sv/net/aspose.words.fields/field/remove/
---
## Field.Remove method

Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista child av dess överordnade nod, returnerar dess överordnade stycke. Om fältet redan är borttaget, returneras`null` .

```csharp
public Node Remove()
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

Visar hur man bearbetar PRIVATA fält.

```csharp
public void FieldPrivate()
{
    // Öppna ett Corel WordPerfect-dokument som vi har konverterat till .docx-format.
    Document doc = new Document(MyDir + "Field sample - PRIVATE.docx");

    // WordPerfect 5.x/6.x-dokument som det vi har laddat kan innehålla PRIVATA fält.
    // Microsoft Word bevarar PRIVATA fält under laddnings-/sparaoperationer,
    // men ger dem ingen funktionalitet.
    FieldPrivate field = (FieldPrivate)doc.Range.Fields[0];

    Assert.AreEqual(" PRIVATE \"My value\" ", field.GetFieldCode());
    Assert.AreEqual(FieldType.FieldPrivate, field.Type);

    // Vi kan också infoga PRIVATA fält med hjälp av en dokumentbyggare.
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(FieldType.FieldPrivate, true);

    // Dessa fält är inte ett gångbart sätt att skydda känslig information.
    // Om inte bakåtkompatibilitet med äldre versioner av WordPerfect är avgörande,
    // vi kan säkert ta bort dessa fält. Vi kan göra detta med hjälp av en DocumentVisiitor-implementering.
    Assert.AreEqual(2, doc.Range.Fields.Count);

    FieldPrivateRemover remover = new FieldPrivateRemover();
    doc.Accept(remover);

    Assert.AreEqual(2, remover.GetFieldsRemovedCount());
    Assert.AreEqual(0, doc.Range.Fields.Count);
}

/// <summary>
/// Tar bort alla påträffade PRIVATA fält.
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
    /// Anropas när en FieldEnd-nod påträffas i dokumentet.
    /// Om noden tillhör ett PRIVAT fält tas hela fältet bort.
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

### Se även

* class [Node](../../../aspose.words/node/)
* class [Field](../)
* namnutrymme [Aspose.Words.Fields](../../field/)
* hopsättning [Aspose.Words](../../../)


