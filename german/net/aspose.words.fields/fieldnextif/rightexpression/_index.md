---
title: FieldNextIf.RightExpression
linktitle: RightExpression
articleTitle: RightExpression
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „FieldNextIf RightExpression“, um die rechte Seite Ihrer Vergleichsausdrücke für eine verbesserte Datenverarbeitung einfach zu verwalten und anzupassen.
type: docs
weight: 40
url: /de/net/aspose.words.fields/fieldnextif/rightexpression/
---
## FieldNextIf.RightExpression property

Ruft den rechten Teil des Vergleichsausdrucks ab oder legt ihn fest.

```csharp
public string RightExpression { get; set; }
```

## Beispiele

Zeigt, wie Sie NEXT/NEXTIF-Felder verwenden, um während eines Seriendrucks mehrere Zeilen zu einer Seite zusammenzuführen.

```csharp
public void FieldNext()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Erstellen Sie eine Datenquelle für unseren Serienbrief mit 3 Zeilen.
    // Ein Serienbrief, der diese Tabelle verwendet, würde normalerweise ein 3-seitiges Dokument erstellen.
    DataTable table = new DataTable("Employees");
    table.Columns.Add("Courtesy Title");
    table.Columns.Add("First Name");
    table.Columns.Add("Last Name");
    table.Rows.Add("Mr.", "John", "Doe");
    table.Rows.Add("Mrs.", "Jane", "Cardholder");
    table.Rows.Add("Mr.", "Joe", "Bloggs");

    InsertMergeFields(builder, "First row: ");

    // Wenn wir mehrere Seriendruckfelder mit demselben Feldnamen haben,
    // Sie erhalten Daten aus derselben Zeile der Datenquelle und zeigen nach der Zusammenführung denselben Wert an.
    // Ein NEXT-Feld weist den Serienbrief sofort an, eine Zeile nach unten zu gehen,
    // was bedeutet, dass alle MERGEFIELDs, die auf das NEXT-Feld folgen, Daten aus der nächsten Zeile erhalten.
    // Achten Sie darauf, niemals zu versuchen, zur nächsten Zeile zu springen, während Sie sich bereits in der letzten Zeile befinden.
    FieldNext fieldNext = (FieldNext)builder.InsertField(FieldType.FieldNext, true);

    Assert.AreEqual(" NEXT ", fieldNext.GetFieldCode());

    // Nach der Zusammenführung werden die Datenquellenwerte, die diese MERGEFIELDs akzeptieren
        // landet auf derselben Seite wie die MERGEFIELDs oben.
    InsertMergeFields(builder, "Second row: ");

    // Ein NEXTIF-Feld hat die gleiche Funktion wie ein NEXT-Feld,
    // aber es wird nur dann zur nächsten Zeile gesprungen, wenn eine aus den folgenden 3 Eigenschaften erstellte Anweisung wahr ist.
    FieldNextIf fieldNextIf = (FieldNextIf)builder.InsertField(FieldType.FieldNextIf, true);
    fieldNextIf.LeftExpression = "5";
    fieldNextIf.RightExpression = "2 + 3";
    fieldNextIf.ComparisonOperator = "=";

    Assert.AreEqual(" NEXTIF  5 = \"2 + 3\"", fieldNextIf.GetFieldCode());

    // Wenn der durch das obige Feld bestätigte Vergleich korrekt ist,
    // Die folgenden 3 Seriendruckfelder übernehmen Daten aus der dritten Zeile.
    // Andernfalls übernehmen diese Felder erneut Daten aus Zeile 2.
    InsertMergeFields(builder, "Third row: ");

    doc.MailMerge.Execute(table);

        // Unsere Datenquelle hat 3 Zeilen und wir haben zweimal Zeilen übersprungen.
    // Unser Ausgabedokument besteht aus 1 Seite mit Daten aus allen 3 Zeilen.
    doc.Save(ArtifactsDir + "Field.NEXT.NEXTIF.docx");
}

/// <summary>
/// Verwendet einen Dokumentgenerator, um MERGEFIELDs für eine Datenquelle einzufügen, die Spalten mit den Namen „Anrede“, „Vorname“ und „Nachname“ enthält.
/// </summary>
public void InsertMergeFields(DocumentBuilder builder, string firstFieldTextBefore)
{
    InsertMergeField(builder, "Courtesy Title", firstFieldTextBefore, " ");
    InsertMergeField(builder, "First Name", null, " ");
    InsertMergeField(builder, "Last Name", null, null);
    builder.InsertParagraph();
}

/// <summary>
/// Verwendet einen Dokumentgenerator, um ein MERRGEFIELD mit angegebenen Eigenschaften einzufügen.
/// </summary>
public void InsertMergeField(DocumentBuilder builder, string fieldName, string textBefore, string textAfter)
{
    FieldMergeField field = (FieldMergeField) builder.InsertField(FieldType.FieldMergeField, true);
    field.FieldName = fieldName;
    field.TextBefore = textBefore;
    field.TextAfter = textAfter;
}
```

### Siehe auch

* class [FieldNextIf](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
