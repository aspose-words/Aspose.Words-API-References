---
title: Class FieldMergeSeq
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fields.FieldMergeSeq klas. Implementiert das MERGESEQFeld.
type: docs
weight: 2020
url: /de/net/aspose.words.fields/fieldmergeseq/
---
## FieldMergeSeq class

Implementiert das MERGESEQ-Feld.

```csharp
public class FieldMergeSeq : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldMergeSeq](fieldmergeseq/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format/) { get; } | erhält a[`FieldFormat`](../fieldformat/) Objekt, das typisierten Zugriff auf die Feldformatierung bereitstellt. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Liest oder setzt Text, der zwischen dem Feldtrennzeichen und dem Feldende steht. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann null sein. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern sind enthalten. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Gibt Text zwischen Feldanfang und Feldtrennzeichen (oder Feldende, wenn kein Trennzeichen vorhanden ist) zurück. |
| [Remove](../../aspose.words.fields/field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte Kind seines Elternknotens ist, wird sein Elternabsatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben **Null** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Führt das Feld Unlink aus. |
| [Update](../../aspose.words.fields/field/update/)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

### Bemerkungen

Im Moment implementieren die Felder MERGEREC und MERGESEQ die gleiche Funktionalität, weil wir nicht genau wissen, wie Datensätze im Seriendruck von Aspose.Words übersprungen werden.

### Beispiele

Zeigt, wie die Felder MERGEREC und MERGESEQ verwendet werden, um Seriendruckdatensätze in den Ausgabedokumenten eines Seriendrucks zu nummerieren und zu zählen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(",");

// Ein MERGEREC-Feld gibt die Zeilennummer der zusammenzuführenden Daten in jedem Zusammenführungsausgabedokument aus.
builder.Write("\nRow number of record in data source: ");
FieldMergeRec fieldMergeRec = (FieldMergeRec)builder.InsertField(FieldType.FieldMergeRec, true);

Assert.AreEqual(" MERGEREC ", fieldMergeRec.GetFieldCode());

// Ein MERGESEQ-Feld zählt die Anzahl erfolgreicher Zusammenführungen und gibt den aktuellen Wert auf jeder entsprechenden Seite aus.
// Wenn ein Seriendruck keine Zeilen überspringt und keine SKIP/SKIPIF/NEXT/NEXTIF-Felder aufruft, sind alle Zusammenführungen erfolgreich.
// Die Felder MERGESEQ und MERGEREC zeigen die gleichen Ergebnisse ihres erfolgreichen Seriendrucks an.
builder.Write("\nSuccessful merge number: ");
FieldMergeSeq fieldMergeSeq = (FieldMergeSeq)builder.InsertField(FieldType.FieldMergeSeq, true);

Assert.AreEqual(" MERGESEQ ", fieldMergeSeq.GetFieldCode());

// Füge ein SKIPIF-Feld ein, das eine Zusammenführung überspringt, wenn der Name "John Doe" ist.
FieldSkipIf fieldSkipIf = (FieldSkipIf)builder.InsertField(FieldType.FieldSkipIf, true);
builder.MoveTo(fieldSkipIf.Separator);
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "John Doe";

// Erstellen Sie eine Datenquelle mit 3 Zeilen, von denen eine "John Doe" als Wert für die Spalte "Name" enthält.
// Da ein SKIPIF-Feld einmal durch diesen Wert ausgelöst wird, hat die Ausgabe unseres Seriendrucks 2 statt 3 Seiten.
// Auf Seite 1 zeigen die Felder MERGESEQ und MERGEREC beide "1" an.
// Auf Seite 2 zeigt das MERGEREC-Feld "3" und das MERGESEQ-Feld "2" an.
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


