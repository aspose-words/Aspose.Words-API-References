---
title: FieldSkipIf Class
linktitle: FieldSkipIf
articleTitle: FieldSkipIf
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fields.FieldSkipIf, um SKIPIF-Felder effizient zu implementieren und so die Dokumentenautomatisierung und Flexibilität in Ihren Projekten zu verbessern.
type: docs
weight: 2830
url: /de/net/aspose.words.fields/fieldskipif/
---
## FieldSkipIf class

Implementiert das SKIPIF-Feld.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class FieldSkipIf : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldSkipIf](fieldskipif/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/fieldskipif/comparisonoperator/) { get; set; } | Ruft den Vergleichsoperator ab oder legt ihn fest. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Erhält eine[`FieldFormat`](../fieldformat/)Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (das Ergebnis sollte nicht neu berechnet werden). |
| [LeftExpression](../../aspose.words.fields/fieldskipif/leftexpression/) { get; set; } | Ruft den linken Teil des Vergleichsausdrucks ab oder legt ihn fest. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ruft Text ab oder legt ihn fest, der zwischen Feldtrennzeichen und Feldende steht. |
| [RightExpression](../../aspose.words.fields/fieldskipif/rightexpression/) { get; set; } | Ruft den rechten Teil des Vergleichsausdrucks ab oder legt ihn fest. |
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

Vergleicht die durch die Ausdrücke bezeichneten Werte[`LeftExpression`](./leftexpression/) Und[`RightExpression`](./rightexpression/) im Vergleich mit dem Operator bezeichnet durch[`ComparisonOperator`](./comparisonoperator/) . Wenn der Vergleich wahr ist, bricht SKIPIF das aktuelle Merge-Dokument ab, wechselt zum nächsten Datensatz in der Datenquelle und beginnt ein neues Merge-Dokument. Wenn der Vergleich falsch ist, wird das aktuelle Merge-Dokument fortgesetzt.

## Beispiele

Zeigt, wie Sie mithilfe des Felds SKIPIF Seiten in einem Serienbrief überspringen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügt ein SKIPIF-Feld ein. Wenn die aktuelle Zeile einer Serienbriefoperation die Bedingung erfüllt
// was die Ausdrücke dieses Feldes angeben, dann bricht der Serienbriefvorgang die aktuelle Zeile ab,
// verwirft das aktuelle Zusammenführungsdokument und wechselt dann sofort zur nächsten Zeile, um mit dem nächsten Zusammenführungsdokument zu beginnen.
FieldSkipIf fieldSkipIf = (FieldSkipIf) builder.InsertField(FieldType.FieldSkipIf, true);

// Verschieben Sie den Builder zum Trennzeichen des SKIPIF-Felds, damit wir ein MERGEFIELD innerhalb des SKIPIF-Felds platzieren können.
builder.MoveTo(fieldSkipIf.Separator);
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Department";

// Das MERGEFIELD bezieht sich auf die Spalte "Abteilung" in unserer Datentabelle. Wenn eine Zeile aus dieser Tabelle
// hat in der Spalte „Abteilung“ den Wert „HR“, dann erfüllt diese Zeile die Bedingung.
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "HR";

// Fügen Sie unserem Dokument Inhalt hinzu, erstellen Sie die Datenquelle und führen Sie den Serienbrief aus.
builder.MoveToDocumentEnd();
builder.Write("Dear ");
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(", ");

    // Diese Tabelle hat drei Zeilen und eine davon erfüllt die Bedingung unseres SKIPIF-Felds.
// Der Serienbrief erzeugt zwei Seiten.
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Columns.Add("Department");
table.Rows.Add("John Doe", "Sales");
table.Rows.Add("Jane Doe", "Accounting");
table.Rows.Add("John Cardholder", "HR");

doc.MailMerge.Execute(table);
doc.Save(ArtifactsDir + "Field.SKIPIF.docx");
```

Zeigt, wie die Felder MERGEREC und MERGESEQ zum Nummerieren und Zählen von Serienbriefdatensätzen in den Ausgabedokumenten eines Serienbriefs verwendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(",");

// Ein MERGEREC-Feld druckt die Zeilennummer der zusammengeführten Daten in jedem Zusammenführungsausgabedokument.
builder.Write("\nRow number of record in data source: ");
FieldMergeRec fieldMergeRec = (FieldMergeRec)builder.InsertField(FieldType.FieldMergeRec, true);

Assert.AreEqual(" MERGEREC ", fieldMergeRec.GetFieldCode());

// Ein MERGESEQ-Feld zählt die Anzahl der erfolgreichen Zusammenführungen und druckt den aktuellen Wert auf der jeweiligen Seite.
// Wenn bei einem Serienbrief keine Zeilen übersprungen werden und keine SKIP/SKIPIF/NEXT/NEXTIF-Felder aufgerufen werden, sind alle Serienbriefe erfolgreich.
// Die Felder MERGESEQ und MERGEREC zeigen die gleichen Ergebnisse an, wenn der Seriendruck erfolgreich war.
builder.Write("\nSuccessful merge number: ");
FieldMergeSeq fieldMergeSeq = (FieldMergeSeq)builder.InsertField(FieldType.FieldMergeSeq, true);

Assert.AreEqual(" MERGESEQ ", fieldMergeSeq.GetFieldCode());

// Fügen Sie ein SKIPIF-Feld ein, das eine Zusammenführung überspringt, wenn der Name „John Doe“ lautet.
FieldSkipIf fieldSkipIf = (FieldSkipIf)builder.InsertField(FieldType.FieldSkipIf, true);
builder.MoveTo(fieldSkipIf.Separator);
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "John Doe";

// Erstellen Sie eine Datenquelle mit 3 Zeilen, von denen eine „John Doe“ als Wert für die Spalte „Name“ enthält.
// Da ein SKIPIF-Feld einmal durch diesen Wert ausgelöst wird, besteht die Ausgabe unseres Serienbriefs aus 2 statt 3 Seiten.
// Auf Seite 1 zeigen die Felder MERGESEQ und MERGEREC beide „1“ an.
// Auf Seite 2 zeigt das Feld MERGEREC „3“ und das Feld MERGESEQ „2“ an.
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Rows.Add("Jane Doe");
table.Rows.Add("John Doe");
table.Rows.Add("Joe Bloggs");

doc.MailMerge.Execute(table);
doc.Save(ArtifactsDir + "Field.MERGEREC.MERGESEQ.docx");
```

### Siehe auch

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
