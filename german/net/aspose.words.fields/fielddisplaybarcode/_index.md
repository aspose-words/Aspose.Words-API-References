---
title: FieldDisplayBarcode Class
linktitle: FieldDisplayBarcode
articleTitle: FieldDisplayBarcode
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words.Fields.FieldDisplayBarcode-Klasse, um mühelos DISPLAYBARCODE-Felder in Ihre Dokumente zu implementieren. Optimieren Sie Ihr Dokumentenmanagement noch heute!
type: docs
weight: 2210
url: /de/net/aspose.words.fields/fielddisplaybarcode/
---
## FieldDisplayBarcode class

Implementiert das Feld DISPLAYBARCODE.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class FieldDisplayBarcode : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldDisplayBarcode](fielddisplaybarcode/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AddStartStopChar](../../aspose.words.fields/fielddisplaybarcode/addstartstopchar/) { get; set; } | Ruft ab oder legt fest, ob Start-/Stoppzeichen für die Barcodetypen NW7 und CODE39 hinzugefügt werden sollen. |
| [BackgroundColor](../../aspose.words.fields/fielddisplaybarcode/backgroundcolor/) { get; set; } | Ruft die Hintergrundfarbe des Barcode-Symbols ab oder legt sie fest. Gültige Werte liegen im Bereich [0, 0xFFFFFF] |
| [BarcodeType](../../aspose.words.fields/fielddisplaybarcode/barcodetype/) { get; set; } | Ruft den Barcode-Typ (QR usw.) ab oder legt ihn fest. |
| [BarcodeValue](../../aspose.words.fields/fielddisplaybarcode/barcodevalue/) { get; set; } | Ruft den Barcodewert ab oder legt ihn fest. |
| [CaseCodeStyle](../../aspose.words.fields/fielddisplaybarcode/casecodestyle/) { get; set; } | Ruft den Stil eines Case Codes für den Barcode-Typ ITF14 ab oder legt ihn fest. Die gültigen Werte sind [STD&#x7C;EXT&#x7C;ADD] |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [DisplayText](../../aspose.words.fields/fielddisplaybarcode/displaytext/) { get; set; } | Ruft ab oder legt fest, ob Barcode-Daten (Text) zusammen mit dem Bild angezeigt werden sollen. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [ErrorCorrectionLevel](../../aspose.words.fields/fielddisplaybarcode/errorcorrectionlevel/) { get; set; } | Ruft die Fehlerkorrekturstufe des QR-Codes ab oder legt sie fest. Gültige Werte sind [0, 3]. |
| [FixCheckDigit](../../aspose.words.fields/fielddisplaybarcode/fixcheckdigit/) { get; set; } | Ruft ab oder legt fest, ob die Prüfziffer korrigiert werden soll, wenn sie ungültig ist. |
| [ForegroundColor](../../aspose.words.fields/fielddisplaybarcode/foregroundcolor/) { get; set; } | Ruft die Vordergrundfarbe des Barcode-Symbols ab oder legt sie fest. Gültige Werte liegen im Bereich [0, 0xFFFFFF] |
| [Format](../../aspose.words.fields/field/format/) { get; } | Erhält eine[`FieldFormat`](../fieldformat/)Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (das Ergebnis sollte nicht neu berechnet werden). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [PosCodeStyle](../../aspose.words.fields/fielddisplaybarcode/poscodestyle/) { get; set; } | Ruft den Stil eines Point-of-Sale-Barcodes ab oder legt ihn fest (Barcodetypen UPCA&#x7C;UPCE&#x7C;EAN13&#x7C;EAN8). Die gültigen Werte (ohne Berücksichtigung der Groß-/Kleinschreibung) sind [STD&#x7C;SUP2&#x7C;SUP5&#x7C;CASE]. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ruft Text ab oder legt ihn fest, der zwischen Feldtrennzeichen und Feldende steht. |
| [ScalingFactor](../../aspose.words.fields/fielddisplaybarcode/scalingfactor/) { get; set; } | Ruft einen Skalierungsfaktor für das Symbol ab oder legt ihn fest. Der Wert wird in ganzen Prozentpunkten angegeben. Die gültigen Werte sind [10, 1000] |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann sein`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| [SymbolHeight](../../aspose.words.fields/fielddisplaybarcode/symbolheight/) { get; set; } | Ruft die Höhe des Symbols ab oder legt sie fest. Die Einheit ist TWIPS (1/1440 Zoll). |
| [SymbolRotation](../../aspose.words.fields/fielddisplaybarcode/symbolrotation/) { get; set; } | Ruft die Rotation des Barcodesymbols ab oder legt sie fest. Gültige Werte sind [0, 3] |
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

Fügt einen Barcode ein.

## Beispiele

Zeigt, wie ein Serienbrief mit QR-Barcodes erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein MERGEBARCODE-Feld ein, das während eines Serienbriefs Werte aus einer Datenquelle akzeptiert.
// Dieses Feld konvertiert alle Werte in der Spalte „MyQRCode“ einer zusammengeführten Datenquelle in QR-Codes.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "QR";
field.BarcodeValue = "MyQRCode";

// Benutzerdefinierte Farben und Skalierung anwenden.
field.BackgroundColor = "0xF8BD69";
field.ForegroundColor = "0xB5413B";
field.ErrorCorrectionLevel = "3";
field.ScalingFactor = "250";
field.SymbolHeight = "1000";
field.SymbolRotation = "0";

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyQRCode QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0",
    field.GetFieldCode());
builder.Writeln();

// Erstellen Sie eine DataTable mit einer Spalte mit demselben Namen wie der BarcodeValue unseres MERGEBARCODE-Felds.
// Der Serienbrief erstellt für jede Zeile eine neue Seite. Jede Seite enthält ein DISPLAYBARCODE-Feld.
// wodurch ein QR-Code mit dem Wert aus der zusammengeführte Zeile angezeigt wird.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyQRCode");
table.Rows.Add(new[] { "ABC123" });
table.Rows.Add(new[] { "DEF456" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"ABC123\" QR \\q 3 \\s 250 \\h 1000 \\r 0 \\b 0xF8BD69 \\f 0xB5413B", 
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"DEF456\" QR \\q 3 \\s 250 \\h 1000 \\r 0 \\b 0xF8BD69 \\f 0xB5413B",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.QR.docx");
```

Zeigt, wie ein DISPLAYBARCODE-Feld eingefügt und seine Eigenschaften festgelegt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDisplayBarcode field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);

// Unten sind vier Arten von Barcodes aufgeführt, die auf verschiedene Weise gestaltet sind und die das Feld DISPLAYBARCODE anzeigen kann.
// 1 - QR-Code mit benutzerdefinierten Farben:
field.BarcodeType = "QR";
field.BarcodeValue = "ABC123";
field.BackgroundColor = "0xF8BD69";
field.ForegroundColor = "0xB5413B";
field.ErrorCorrectionLevel = "3";
field.ScalingFactor = "250";
field.SymbolHeight = "1000";
field.SymbolRotation = "0";

Assert.AreEqual(" DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0", field.GetFieldCode());
builder.Writeln();

// 2 - EAN13-Barcode, mit den unter den Balken angezeigten Ziffern:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "501234567890";
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// 3 - CODE39-Barcode:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "12345ABCDE";
field.AddStartStopChar = true;

Assert.AreEqual(" DISPLAYBARCODE  12345ABCDE CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// 4 - ITF4-Barcode mit einem angegebenen Fallcode:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "09312345678907";
field.CaseCodeStyle = "STD";

Assert.AreEqual(" DISPLAYBARCODE  09312345678907 ITF14 \\c STD", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.DISPLAYBARCODE.docx");
```

### Siehe auch

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
