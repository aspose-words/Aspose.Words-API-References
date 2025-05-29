---
title: FieldSkipIf.RightExpression
linktitle: RightExpression
articleTitle: RightExpression
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „FieldSkipIf RightExpression“ und verwalten Sie Vergleichsausdrücke ganz einfach für eine verbesserte Datenkontrolle und optimierte Vorgänge.
type: docs
weight: 40
url: /de/net/aspose.words.fields/fieldskipif/rightexpression/
---
## FieldSkipIf.RightExpression property

Ruft den rechten Teil des Vergleichsausdrucks ab oder legt ihn fest.

```csharp
public string RightExpression { get; set; }
```

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

* class [FieldSkipIf](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
