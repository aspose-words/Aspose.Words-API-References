---
title: FieldSkipIf.ComparisonOperator
second_title: Aspose.Words für .NET-API-Referenz
description: FieldSkipIf eigendom. Ruft den Vergleichsoperator ab oder legt ihn fest.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldskipif/comparisonoperator/
---
## FieldSkipIf.ComparisonOperator property

Ruft den Vergleichsoperator ab oder legt ihn fest.

```csharp
public string ComparisonOperator { get; set; }
```

### Beispiele

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

* class [FieldSkipIf](../)
* namensraum [Aspose.Words.Fields](../../fieldskipif/)
* Montage [Aspose.Words](../../../)


