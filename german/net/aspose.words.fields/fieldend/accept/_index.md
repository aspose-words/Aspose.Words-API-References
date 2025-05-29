---
title: FieldEnd.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words für .NET
description: Entdecken Sie die Accept-Methode von FieldEnd – binden Sie Besucher nahtlos ein und verbessern Sie das Benutzererlebnis mit unseren innovativen Lösungen. Schöpfen Sie noch heute das Potenzial Ihrer Website aus!
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldend/accept/
---
## FieldEnd.Accept method

Nimmt einen Besucher auf.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| visitor | DocumentVisitor | Der Besucher, der den Knoten besuchen wird. |

### Rückgabewert

**FALSCH** wenn der Besucher die Beendigung der Aufzählung verlangt hat.

## Bemerkungen

Anrufe[`VisitFieldEnd`](../../../aspose.words/documentvisitor/visitfieldend/).

Weitere Informationen finden Sie im Besucher-Entwurfsmuster.

## Beispiele

Zeigt, wie mit einer Sammlung von Feldern gearbeitet wird.

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

    // Durchlaufen Sie die Feldsammlung und drucken Sie Inhalt und Typ
    // jedes Felds mithilfe einer benutzerdefinierten Besucherimplementierung.
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
/// Dokumentieren Sie die Besucherimplementierung, die Feldinformationen druckt.
/// </summary>
public class FieldVisitor : DocumentVisitor
{
    public FieldVisitor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Ruft den Klartext des vom Besucher gesammelten Dokuments ab.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein FieldStart-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        mBuilder.AppendLine("Found field: " + fieldStart.FieldType);
        mBuilder.AppendLine("\tField code: " + fieldStart.GetField().GetFieldCode());
        mBuilder.AppendLine("\tDisplayed as: " + fieldStart.GetField().Result);

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein FieldSeparator-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        mBuilder.AppendLine("\tFound separator: " + fieldSeparator.GetText());

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein FieldEnd-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mBuilder.AppendLine("End of field: " + fieldEnd.FieldType);

        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
}
```

### Siehe auch

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [FieldEnd](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
