---
title: FieldDisplayBarcode
second_title: Aspose.Words für .NET-API-Referenz
description: Implementiert das Feld DISPLAYBARCODE.
type: docs
weight: 1650
url: /de/net/aspose.words.fields/fielddisplaybarcode/
---
## FieldDisplayBarcode class

Implementiert das Feld DISPLAYBARCODE.

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
| [AddStartStopChar](../../aspose.words.fields/fielddisplaybarcode/addstartstopchar/) { get; set; } | Ruft ab oder legt fest, ob Start-/Stoppzeichen für Barcodetypen NW7 und CODE39 hinzugefügt werden sollen. |
| [BackgroundColor](../../aspose.words.fields/fielddisplaybarcode/backgroundcolor/) { get; set; } | Liest oder setzt die Hintergrundfarbe des Barcode-Symbols. Gültige Werte liegen im Bereich [0, 0xFFFFFF] |
| [BarcodeType](../../aspose.words.fields/fielddisplaybarcode/barcodetype/) { get; set; } | Liest oder setzt den Barcode-Typ (QR, etc.) |
| [BarcodeValue](../../aspose.words.fields/fielddisplaybarcode/barcodevalue/) { get; set; } | Ruft den Barcodewert ab oder legt ihn fest. |
| [CaseCodeStyle](../../aspose.words.fields/fielddisplaybarcode/casecodestyle/) { get; set; } | Ruft den Stil eines Fallcodes für den Barcodetyp ITF14 ab oder legt ihn fest. Die gültigen Werte sind [STD&#x7C;EXT&#x7C;ADD] |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [DisplayText](../../aspose.words.fields/fielddisplaybarcode/displaytext/) { get; set; } | Ruft ab oder legt fest, ob Barcode-Daten (Text) zusammen mit dem Bild angezeigt werden sollen. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [ErrorCorrectionLevel](../../aspose.words.fields/fielddisplaybarcode/errorcorrectionlevel/) { get; set; } | Ruft eine Fehlerkorrekturstufe des QR-Codes ab oder legt sie fest. Gültige Werte sind [0, 3]. |
| [FixCheckDigit](../../aspose.words.fields/fielddisplaybarcode/fixcheckdigit/) { get; set; } | Ruft ab oder legt fest, ob die Prüfziffer korrigiert werden soll, wenn sie ungültig ist. |
| [ForegroundColor](../../aspose.words.fields/fielddisplaybarcode/foregroundcolor/) { get; set; } | Ermittelt oder setzt die Vordergrundfarbe des Barcode-Symbols. Gültige Werte liegen im Bereich [0, 0xFFFFFF] |
| [Format](../../aspose.words.fields/field/format/) { get; } | erhält a[`FieldFormat`](../fieldformat/) Objekt, das typisierten Zugriff auf die Feldformatierung bereitstellt. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [PosCodeStyle](../../aspose.words.fields/fielddisplaybarcode/poscodestyle/) { get; set; } | Ruft den Stil eines Point-of-Sale-Barcodes ab oder legt ihn fest (Barcodetypen UPCA&#x7C;UPCE&#x7C;EAN13&#x7C;EAN8). Die gültigen Werte (Groß-/Kleinschreibung wird nicht beachtet) sind [STD&#x7C;SUP2&#x7C;SUP5&#x7C;CASE]. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Liest oder setzt Text, der zwischen dem Feldtrennzeichen und dem Feldende steht. |
| [ScalingFactor](../../aspose.words.fields/fielddisplaybarcode/scalingfactor/) { get; set; } | Holt oder setzt einen Skalierungsfaktor für das Symbol. Der Wert wird in ganzen Prozentpunkten angegeben und die gültigen Werte sind [10, 1000] |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann null sein. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| [SymbolHeight](../../aspose.words.fields/fielddisplaybarcode/symbolheight/) { get; set; } | Holt oder setzt die Höhe des Symbols. Die Einheiten sind in TWIPS (1/1440 Zoll). |
| [SymbolRotation](../../aspose.words.fields/fielddisplaybarcode/symbolrotation/) { get; set; } | Ermittelt oder setzt die Drehung des Barcode-Symbols. Gültige Werte sind [0, 3] |
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

Fügt einen Barcode ein.

### Beispiele

Zeigt, wie Sie einen Seriendruck für QR-Barcodes durchführen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein MERGEBARCODE-Feld ein, das während eines Seriendrucks Werte aus einer Datenquelle akzeptiert.
// Dieses Feld konvertiert alle Werte in der Spalte „MyQRCode“ einer Zusammenführungsdatenquelle in QR-Codes.
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
// Der Seriendruck erstellt für jede Zeile eine neue Seite. Jede Seite enthält ein DISPLAYBARCODE-Feld,
// wodurch ein QR-Code mit dem Wert aus der zusammengeführten Zeile angezeigt wird.
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

// Unten sind vier Arten von Strichcodes, die auf verschiedene Arten dekoriert sind und die das DISPLAYBARCODE-Feld anzeigen kann.
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

// 2 - EAN13-Barcode, wobei die Ziffern unter den Balken angezeigt werden:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "501234567890";
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// 3 - CODE39-Strichcode:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "12345ABCDE";
field.AddStartStopChar = true;

Assert.AreEqual(" DISPLAYBARCODE  12345ABCDE CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// 4 - ITF4-Barcode mit einem bestimmten Fallcode:
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
