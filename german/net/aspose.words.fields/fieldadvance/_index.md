---
title: FieldAdvance Class
linktitle: FieldAdvance
articleTitle: FieldAdvance
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fields.FieldAdvance für die nahtlose ADVANCE-Feldimplementierung und verbessern Sie mühelos Ihre Dokumentverarbeitungsfunktionen.
type: docs
weight: 1950
url: /de/net/aspose.words.fields/fieldadvance/
---
## FieldAdvance class

Implementiert das ADVANCE-Feld.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class FieldAdvance : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldAdvance](fieldadvance/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [DownOffset](../../aspose.words.fields/fieldadvance/downoffset/) { get; set; } | Ruft die Anzahl der Punkte ab oder legt sie fest, um die der Text, der dem Feld folgt, nach unten verschoben werden soll. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Erhält eine[`FieldFormat`](../fieldformat/)Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [HorizontalPosition](../../aspose.words.fields/fieldadvance/horizontalposition/) { get; set; } | Ruft die Anzahl der Punkte ab oder legt sie fest, um die der Text, der dem Feld folgt, horizontal vom linken Rand der Spalte, des Rahmens oder des Textfelds verschoben werden soll. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (das Ergebnis sollte nicht neu berechnet werden). |
| [LeftOffset](../../aspose.words.fields/fieldadvance/leftoffset/) { get; set; } | Ruft die Anzahl der Punkte ab oder legt sie fest, um die der Text, der dem Feld folgt, nach links verschoben werden soll. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ruft Text ab oder legt ihn fest, der zwischen Feldtrennzeichen und Feldende steht. |
| [RightOffset](../../aspose.words.fields/fieldadvance/rightoffset/) { get; set; } | Ruft die Anzahl der Punkte ab oder legt sie fest, um die der Text, der dem Feld folgt, nach rechts verschoben werden soll. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann sein`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |
| [UpOffset](../../aspose.words.fields/fieldadvance/upoffset/) { get; set; } | Ruft die Anzahl der Punkte ab oder legt sie fest, um die der Text, der dem Feld folgt, nach oben verschoben werden soll. |
| [VerticalPosition](../../aspose.words.fields/fieldadvance/verticalposition/) { get; set; } | Ruft die Anzahl der Punkte ab oder legt sie fest, um die der Text, der dem Feld folgt, vertikal vom oberen Rand der Seite verschoben werden soll. |

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

Verschiebt den Startpunkt, an dem der Text, der dem Feld lexikalisch folgt, angezeigt wird, nach rechts oder links, nach oben oder unten oder an eine bestimmte horizontale oder vertikale Position.

## Beispiele

Zeigt, wie Sie ein ADVANCE-Feld einfügen und seine Eigenschaften bearbeiten.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This text is in its normal place.");

// Unten sind zwei Möglichkeiten aufgeführt, wie Sie mit dem Feld ADVANCE die Position des darauf folgenden Textes anpassen können.
// Die Auswirkungen eines ADVANCE-Feldes bleiben bis zum Ende des Absatzes bestehen,
// oder ein anderes ADVANCE-Feld aktualisiert die Offset-/Koordinatenwerte.
// 1 - Geben Sie einen Richtungsversatz an:
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

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
