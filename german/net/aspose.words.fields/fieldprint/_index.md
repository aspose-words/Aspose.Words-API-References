---
title: FieldPrint Class
linktitle: FieldPrint
articleTitle: FieldPrint
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words.Fields.FieldPrint-Klasse für die nahtlose Implementierung von PRINT-Feldern. Verbessern Sie Ihre Dokumentenverarbeitung noch heute mit leistungsstarken Funktionen!
type: docs
weight: 2690
url: /de/net/aspose.words.fields/fieldprint/
---
## FieldPrint class

Implementiert das PRINT-Feld.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class FieldPrint : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldPrint](fieldprint/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Erhält eine[`FieldFormat`](../fieldformat/)Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (das Ergebnis sollte nicht neu berechnet werden). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [PostScriptGroup](../../aspose.words.fields/fieldprint/postscriptgroup/) { get; set; } | Ruft das Zeichenrechteck ab, auf das die PostScript-Anweisungen angewendet werden, oder legt dieses fest. |
| [PrinterInstructions](../../aspose.words.fields/fieldprint/printerinstructions/) { get; set; } | Ruft die druckerspezifischen Steuercodezeichen oder PostScript-Anweisungen ab oder legt diese fest. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ruft Text ab oder legt ihn fest, der zwischen Feldtrennzeichen und Feldende steht. |
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

Eine Anweisung zum Senden der druckerspezifischen Steuercodezeichen an den ausgewählten Drucker , wenn das Dokument gedruckt wird.

## Beispiele

Zeigt das Einfügen eines PRINT-Felds.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("My paragraph");

// Das Feld PRINT kann Anweisungen an den Drucker senden.
FieldPrint field = (FieldPrint)builder.InsertField(FieldType.FieldPrint, true);

// Legen Sie den Bereich fest, in dem der Drucker Anweisungen ausführen soll.
// In diesem Fall ist es der Absatz, der unser PRINT-Feld enthält.
field.PostScriptGroup = "para";

// Wenn wir zum Drucken unseres Dokuments einen Drucker verwenden, der PostScript unterstützt,
// Dieser Befehl färbt den gesamten Bereich, den wir in „field.PostScriptGroup“ angegeben haben, weiß.
field.PrinterInstructions = "erasepage";

Assert.AreEqual(" PRINT  erasepage \\p para", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.PRINT.docx");
```

### Siehe auch

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
