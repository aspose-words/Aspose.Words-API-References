---
title: FieldNext
second_title: Aspose.Words für .NET-API-Referenz
description: Implementiert das NEXT-Feld.
type: docs
weight: 2030
url: /de/net/aspose.words.fields/fieldnext/
---
## FieldNext class

Implementiert das NEXT-Feld.

```csharp
public class FieldNext : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldNext](fieldnext)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format) { get; } | erhält a[`FieldFormat`](../fieldformat) Objekt, das typisierten Zugriff auf die Feldformatierung bereitstellt. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Liest oder setzt Text, der zwischen dem Feldtrennzeichen und dem Feldende steht. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann null sein. |
| [Start](../../aspose.words.fields/field/start) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern sind enthalten. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Gibt Text zwischen Feldanfang und Feldtrennzeichen (oder Feldende, wenn kein Trennzeichen vorhanden ist) zurück. |
| [Remove](../../aspose.words.fields/field/remove)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte Kind seines Elternknotens ist, wird sein Elternabsatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben **Null** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Führt das Feld Unlink aus. |
| [Update](../../aspose.words.fields/field/update)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update)(bool) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

### Bemerkungen

Führt den nächsten Datensatz in das aktuell resultierende zusammengeführte Dokument ein, anstatt ein neues zusammengeführtes Dokument zu beginnen.

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

* class [Field](../field)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
