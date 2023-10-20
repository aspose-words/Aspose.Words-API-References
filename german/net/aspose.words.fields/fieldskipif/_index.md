---
title: FieldSkipIf Class
linktitle: FieldSkipIf
articleTitle: FieldSkipIf
second_title: Aspose.Words für .NET
description: Aspose.Words.Fields.FieldSkipIf klas. Implementiert das SKIPIFFeld in C#.
type: docs
weight: 2420
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
| [Format](../../aspose.words.fields/field/format/) { get; } | Ruft a ab[`FieldFormat`](../fieldformat/) Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [LeftExpression](../../aspose.words.fields/fieldskipif/leftexpression/) { get; set; } | Ruft den linken Teil des Vergleichsausdrucks ab oder legt diesen fest. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ruft Text ab, der zwischen dem Feldtrennzeichen und dem Feldende liegt, oder legt diesen fest. |
| [RightExpression](../../aspose.words.fields/fieldskipif/rightexpression/) { get; set; } | Ruft den rechten Teil des Vergleichsausdrucks ab oder legt diesen fest. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann sein`Null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl der Feldcode als auch das Feldergebnis der untergeordneten Felder sind enthalten. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). |
| [Remove](../../aspose.words.fields/field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte child seines übergeordneten Knotens ist, wird dessen übergeordneter Absatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben`Null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Führt das Feld unlink aus. |
| [Update](../../aspose.words.fields/field/update/)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

## Bemerkungen

Vergleicht die durch die Ausdrücke angegebenen Werte[`LeftExpression`](./leftexpression/) Und[`RightExpression`](./rightexpression/) im Vergleich mit dem durch bezeichneten Operator[`ComparisonOperator`](./comparisonoperator/) . Wenn der Vergleich wahr ist, bricht SKIPIF das aktuelle Zusammenführungsdokument ab, wechselt zum nächsten Datensatz in der Datenquelle und startet ein neues Zusammenführungsdokument. Wenn der Vergleich falsch ist, wird das aktuelle Zusammenführungsdokument fortgesetzt.

## Beispiele

Zeigt, wie Seiten in einem Seriendruck mithilfe des SKIPIF-Felds übersprungen werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein SKIPIF-Feld einfügen. Wenn die aktuelle Zeile eines Serienbriefvorgangs die Bedingung erfüllt
// was die Ausdrücke dieses Feldes angeben, dann bricht der Seriendruckvorgang die aktuelle Zeile ab,
// verwirft das aktuelle Zusammenführungsdokument und wechselt dann sofort zur nächsten Zeile, um mit dem nächsten Zusammenführungsdokument zu beginnen.
FieldSkipIf fieldSkipIf = (FieldSkipIf) builder.InsertField(FieldType.FieldSkipIf, true);

// Verschieben Sie den Builder zum Trennzeichen des SKIPIF-Felds, damit wir ein MERGEFIELD innerhalb des SKIPIF-Felds platzieren können.
builder.MoveTo(fieldSkipIf.Separator);
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Department";

// Das MERGEFIELD bezieht sich auf die Spalte „Abteilung“ in unserer Datentabelle. Wenn eine Zeile aus dieser Tabelle
// in der Spalte „Abteilung“ den Wert „HR“ hat, erfüllt diese Zeile die Bedingung.
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "HR";

// Fügen Sie Inhalt zu unserem Dokument hinzu, erstellen Sie die Datenquelle und führen Sie den Serienbrief aus.
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

Zeigt, wie die Felder MERGEREC und MERGESEQ zur Anzahl und Zählung von Serienbriefdatensätzen in den Ausgabedokumenten eines Serienbriefs verwendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(",");

// Ein MERGEREC-Feld gibt die Zeilennummer der Daten aus, die in jedem Zusammenführungsausgabedokument zusammengeführt werden.
builder.Write("\nRow number of record in data source: ");
FieldMergeRec fieldMergeRec = (FieldMergeRec)builder.InsertField(FieldType.FieldMergeRec, true);

Assert.AreEqual(" MERGEREC ", fieldMergeRec.GetFieldCode());

// Ein MERGESEQ-Feld zählt die Anzahl erfolgreicher Zusammenführungen und gibt den aktuellen Wert auf jeder entsprechenden Seite aus.
// Wenn ein Serienbrief keine Zeilen überspringt und keine SKIP/SKIPIF/NEXT/NEXTIF-Felder aufruft, sind alle Serienbriefe erfolgreich.
// Die Felder MERGESEQ und MERGEREC zeigen die gleichen Ergebnisse an, wenn der Serienbrief erfolgreich war.
builder.Write("\nSuccessful merge number: ");
FieldMergeSeq fieldMergeSeq = (FieldMergeSeq)builder.InsertField(FieldType.FieldMergeSeq, true);

Assert.AreEqual(" MERGESEQ ", fieldMergeSeq.GetFieldCode());

// Ein SKIPIF-Feld einfügen, das eine Zusammenführung überspringt, wenn der Name „John Doe“ ist.
FieldSkipIf fieldSkipIf = (FieldSkipIf)builder.InsertField(FieldType.FieldSkipIf, true);
builder.MoveTo(fieldSkipIf.Separator);
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "John Doe";

// Erstellen Sie eine Datenquelle mit 3 Zeilen, von denen eine „John Doe“ als Wert für die Spalte „Name“ enthält.
// Da ein SKIPIF-Feld einmal durch diesen Wert ausgelöst wird, wird die Ausgabe unseres Seriendrucks 2 Seiten statt 3 haben.
// Auf Seite 1 zeigen die Felder MERGESEQ und MERGEREC beide „1“ an.
// Auf Seite 2 wird im Feld MERGEREC „3“ und im Feld MERGESEQ „2“ angezeigt.
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Rows.Add(new[] { "Jane Doe" });
table.Rows.Add(new[] { "John Doe" });
table.Rows.Add(new[] { "Joe Bloggs" });

doc.MailMerge.Execute(table);            
doc.Save(ArtifactsDir + "Field.MERGEREC.MERGESEQ.docx");
```

### Siehe auch

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
