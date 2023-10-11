---
title: Class FieldCollection
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fields.FieldCollection klas. Eine Sammlung vonField Objekte die die Felder im angegebenen Bereich darstellen.
type: docs
weight: 1690
url: /de/net/aspose.words.fields/fieldcollection/
---
## FieldCollection class

Eine Sammlung von[`Field`](../field/) Objekte, die die Felder im angegebenen Bereich darstellen.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class FieldCollection : IEnumerable<Field>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.fields/fieldcollection/count/) { get; } | Gibt die Anzahl der Felder in der Sammlung zurück. |
| [Item](../../aspose.words.fields/fieldcollection/item/) { get; } | Gibt ein Feld am angegebenen Index zurück. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Clear](../../aspose.words.fields/fieldcollection/clear/)() | Entfernt alle Felder dieser Sammlung aus dem Dokument und aus dieser Sammlung selbst. |
| [GetEnumerator](../../aspose.words.fields/fieldcollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück. |
| [Remove](../../aspose.words.fields/fieldcollection/remove/)(Field) | Entfernt das angegebene Feld aus dieser Sammlung und aus dem Dokument. |
| [RemoveAt](../../aspose.words.fields/fieldcollection/removeat/)(int) | Entfernt ein Feld am angegebenen Index aus dieser Sammlung und aus dem Dokument. |

### Bemerkungen

Eine Instanz dieser Sammlung iteriert Felder, die zu Beginn in den angegebenen Bereich fallen.

Der`FieldCollection` Die Sammlung besitzt nicht die darin enthaltenen Felder, sondern ist lediglich eine Auswahl von Feldern.

Der`FieldCollection` Die Sammlung ist „live“, d. h. Änderungen an den untergeordneten Elementen des Knotens object , aus dem sie erstellt wurde, werden sofort in den von zurückgegebenen Feldern widergespiegelt`FieldCollection` Eigenschaften und Methoden.

### Beispiele

Zeigt, wie Felder aus einer Feldsammlung entfernt werden.

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

// Im Folgenden finden Sie vier Möglichkeiten zum Entfernen von Feldern aus einer Feldsammlung.
// 1 – Ein Feld abrufen, um sich selbst zu entfernen:
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 – Holen Sie sich die Sammlung, um ein Feld zu entfernen, das wir an seine Entfernungsmethode übergeben:
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 – Ein Feld aus einer Sammlung an einem Index entfernen:
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 – Alle Felder auf einmal aus der Sammlung entfernen:
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

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

    // Über die Feldsammlung iterieren und Inhalt und Typ ausgeben
    // jedes Feldes mithilfe einer benutzerdefinierten Besucherimplementierung.
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

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)


