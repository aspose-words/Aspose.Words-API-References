---
title: FieldNextIf.RightExpression
second_title: Aspose.Words für .NET-API-Referenz
description: FieldNextIf eigendom. Holt oder setzt den rechten Teil des Vergleichsausdrucks.
type: docs
weight: 40
url: /de/net/aspose.words.fields/fieldnextif/rightexpression/
---
## FieldNextIf.RightExpression property

Holt oder setzt den rechten Teil des Vergleichsausdrucks.

```csharp
public string RightExpression { get; set; }
```

### Beispiele

Zeigt, wie NEXT/NEXTIF-Felder verwendet werden, um mehrere Zeilen während eines Seriendrucks auf einer Seite zusammenzuführen.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Erstellen Sie eine Datenquelle für unseren Seriendruck mit 3 Zeilen.
    // Ein Seriendruck, der diese Tabelle verwendet, würde normalerweise ein 3-seitiges Dokument erstellen.
    DataTable table = new DataTable("Employees");
    table.Columns.Add("Courtesy Title");
    table.Columns.Add("First Name");
    table.Columns.Add("Last Name");
    table.Rows.Add("Mr.", "John", "Doe");
    table.Rows.Add("Mrs.", "Jane", "Cardholder");
    table.Rows.Add("Mr.", "Joe", "Bloggs");

    InsertMergeFields(builder, "First row: ");

    // Wenn wir mehrere Briefvorlagenfelder mit demselben FieldName haben,
    // Sie erhalten Daten aus derselben Zeile der Datenquelle und zeigen nach der Zusammenführung denselben Wert an.
    // Ein NEXT-Feld weist den Seriendruck sofort an, eine Zeile nach unten zu gehen,
    // was bedeutet, dass alle MERGEFIELDs, die auf das NEXT-Feld folgen, Daten aus der nächsten Zeile erhalten.
    // Stellen Sie sicher, dass Sie niemals versuchen, zur nächsten Zeile zu springen, während Sie sich bereits in der letzten Zeile befinden.
    FieldNext fieldNext = (FieldNext)builder.InsertField(FieldType.FieldNext, true);

    Assert.AreEqual(" NEXT ", fieldNext.GetFieldCode());

    // Nach der Zusammenführung die Datenquellenwerte, die diese MERGEFIELDs akzeptieren
     // wird auf der gleichen Seite wie die obigen MERGEFIELDs landen.
    InsertMergeFields(builder, "Second row: ");

    // Ein NEXTIF-Feld hat die gleiche Funktion wie ein NEXT-Feld,
    // springt aber nur dann zur nächsten Zeile, wenn eine aus den folgenden 3 Eigenschaften konstruierte Aussage wahr ist.
    FieldNextIf fieldNextIf = (FieldNextIf)builder.InsertField(FieldType.FieldNextIf, true);
    fieldNextIf.LeftExpression = "5";
    fieldNextIf.RightExpression = "2 + 3";
    fieldNextIf.ComparisonOperator = "=";

    Assert.AreEqual(" NEXTIF  5 = \"2 + 3\"", fieldNextIf.GetFieldCode());

    // Wenn der durch das obige Feld bestätigte Vergleich korrekt ist,
    // Die folgenden 3 Zusammenführungsfelder übernehmen Daten aus der dritten Zeile.
    // Andernfalls übernehmen diese Felder wieder Daten aus Zeile 2.
    InsertMergeFields(builder, "Third row: ");

    doc.MailMerge.Execute(table);

     // Unsere Datenquelle hat 3 Zeilen und wir haben Zeilen zweimal übersprungen.
    // Unser Ausgabedokument hat 1 Seite mit Daten aus allen 3 Zeilen.
    doc.Save(ArtifactsDir + "Field.NEXT.NEXTIF.docx");

/// <summary>
/// Verwendet einen Document Builder, um MERGEFIELDs für eine Datenquelle einzufügen, die Spalten mit den Namen "Courtesy Title", "First Name" und "Last Name" enthält.
/// </summary>
public void InsertMergeFields(DocumentBuilder builder, string firstFieldTextBefore)
{
    InsertMergeField(builder, "Courtesy Title", firstFieldTextBefore, " ");
    InsertMergeField(builder, "First Name", null, " ");
    InsertMergeField(builder, "Last Name", null, null);
    builder.InsertParagraph();
}

/// <summary>
/// Verwendet einen Document Builder, um ein MERRGEFIELD mit angegebenen Eigenschaften einzufügen.
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
* namensraum [Aspose.Words.Fields](../../fieldnextif/)
* Montage [Aspose.Words](../../../)


