---
title: FieldNextIf Class
linktitle: FieldNextIf
articleTitle: FieldNextIf
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fields.FieldNextIf – implementieren Sie NEXTIF-Felder effizient, um die Dokumentenautomatisierung zu verbessern und Ihre Arbeitsabläufe zu optimieren.
type: docs
weight: 2600
url: /de/net/aspose.words.fields/fieldnextif/
---
## FieldNextIf class

Implementiert das NEXTIF-Feld.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class FieldNextIf : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldNextIf](fieldnextif/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/fieldnextif/comparisonoperator/) { get; set; } | Ruft den Vergleichsoperator ab oder legt ihn fest. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Erhält eine[`FieldFormat`](../fieldformat/)Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (das Ergebnis sollte nicht neu berechnet werden). |
| [LeftExpression](../../aspose.words.fields/fieldnextif/leftexpression/) { get; set; } | Ruft den linken Teil des Vergleichsausdrucks ab oder legt ihn fest. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ruft Text ab oder legt ihn fest, der zwischen Feldtrennzeichen und Feldende steht. |
| [RightExpression](../../aspose.words.fields/fieldnextif/rightexpression/) { get; set; } | Ruft den rechten Teil des Vergleichsausdrucks ab oder legt ihn fest. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann sein`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern werden einbezogen. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). |
| [Remove](../../aspose.words.fields/field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte Kind seines übergeordneten Knotens ist, wird dessen übergeordneter Absatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Führt die Feldverknüpfung aus. |
| [Update](../../aspose.words.fields/field/update/)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

## Bemerkungen

Vergleicht die durch die Ausdrücke bezeichneten Werte[`LeftExpression`](./leftexpression/) Und[`RightExpression`](./rightexpression/) im Vergleich mit dem Operator bezeichnet durch[`ComparisonOperator`](./comparisonoperator/) Wenn der Vergleich wahr ist, wird der nächste Datensatz in das aktuelle Zusammenführungsdokument eingefügt. (Zusammenführungsfelder, die im Hauptdokument auf NEXTIF folgen, werden durch Werte aus dem nächsten Datensatz und nicht aus dem aktuellen Datensatz ersetzt.) Wenn der Vergleich falsch ist, wird der nächste Datensatz in ein neues Zusammenführungsdokument eingefügt.

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

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
