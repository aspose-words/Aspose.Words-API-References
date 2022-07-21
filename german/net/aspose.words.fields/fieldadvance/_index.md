---
title: FieldAdvance
second_title: Aspose.Words für .NET-API-Referenz
description: Implementiert das ADVANCE-Feld.
type: docs
weight: 1390
url: /de/net/aspose.words.fields/fieldadvance/
---
## FieldAdvance class

Implementiert das ADVANCE-Feld.

```csharp
public class FieldAdvance : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldAdvance](fieldadvance)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [DownOffset](../../aspose.words.fields/fieldadvance/downoffset) { get; set; } | Ermittelt oder setzt die Anzahl der Punkte, um die der Text, der dem Feld folgt, nach unten verschoben werden soll. |
| [End](../../aspose.words.fields/field/end) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format) { get; } | erhält a[`FieldFormat`](../fieldformat) Objekt, das typisierten Zugriff auf die Feldformatierung bereitstellt. |
| [HorizontalPosition](../../aspose.words.fields/fieldadvance/horizontalposition) { get; set; } | Ruft die Anzahl der Punkte ab oder legt sie fest, um die der Text, der auf das Feld folgt, horizontal vom linken Rand der Spalte, des Rahmens oder des Textfelds verschoben werden soll. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [LeftOffset](../../aspose.words.fields/fieldadvance/leftoffset) { get; set; } | Ermittelt oder setzt die Anzahl der Punkte, um die der Text, der dem Feld folgt, nach links verschoben werden soll. |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Liest oder setzt Text, der zwischen dem Feldtrennzeichen und dem Feldende steht. |
| [RightOffset](../../aspose.words.fields/fieldadvance/rightoffset) { get; set; } | Ermittelt oder setzt die Anzahl der Punkte, um die der Text, der dem Feld folgt, nach rechts verschoben werden soll. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann null sein. |
| [Start](../../aspose.words.fields/field/start) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Ruft den Microsoft Word-Feldtyp ab. |
| [UpOffset](../../aspose.words.fields/fieldadvance/upoffset) { get; set; } | Ermittelt oder setzt die Anzahl der Punkte, um die der Text, der dem Feld folgt, nach oben verschoben werden soll. |
| [VerticalPosition](../../aspose.words.fields/fieldadvance/verticalposition) { get; set; } | Ermittelt oder setzt die Anzahl der Punkte, um die der Text, der dem Feld folgt, vertikal vom oberen Rand der Seite verschoben werden soll. |

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

Verschiebt den Startpunkt, an dem der Text, der dem Feld lexikalisch folgt, angezeigt wird, nach rechts oder links, nach oben oder unten oder an eine bestimmte horizontale oder vertikale Position.

### Beispiele

Zeigt, wie ein ADVANCE-Feld eingefügt und seine Eigenschaften bearbeitet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This text is in its normal place.");

// Im Folgenden finden Sie zwei Möglichkeiten, das ADVANCE-Feld zu verwenden, um die Position des darauf folgenden Textes anzupassen.
// Die Effekte eines ADVANCE-Feldes werden weiter angewendet, bis der Absatz endet,
// oder ein anderes ADVANCE-Feld aktualisiert die Versatz-/Koordinatenwerte.
// 1 - Geben Sie einen Richtungsoffset an:
FieldAdvance field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.RightOffset = "5";
field.UpOffset = "5";

Assert.AreEqual(" ADVANCE  \\r 5 \\u 5", field.GetFieldCode());

builder.Write("This text will be moved up and to the right.");

field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.DownOffset = "5";
field.LeftOffset = "100";

Assert.AreEqual(" ADVANCE  \\d 5 \\l 100", field.GetFieldCode());

builder.Writeln("This text is moved down and to the left, overlapping the previous text.");

// 2 - Text an eine durch Koordinaten angegebene Position verschieben:
field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.HorizontalPosition = "-100";
field.VerticalPosition = "200";

Assert.AreEqual(" ADVANCE  \\x -100 \\y 200", field.GetFieldCode());

builder.Write("This text is in a custom position.");

doc.Save(ArtifactsDir + "Field.ADVANCE.docx");
```

### Siehe auch

* class [Field](../field)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
