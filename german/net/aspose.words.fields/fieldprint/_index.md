---
title: Class FieldPrint
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fields.FieldPrint klas. Implementiert das PRINTFeld.
type: docs
weight: 2280
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
| [Format](../../aspose.words.fields/field/format/) { get; } | Ruft a ab[`FieldFormat`](../fieldformat/) Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [PostScriptGroup](../../aspose.words.fields/fieldprint/postscriptgroup/) { get; set; } | Ruft das Zeichenrechteck ab, auf das die PostScript-Anweisungen angewendet werden, oder legt dieses fest. |
| [PrinterInstructions](../../aspose.words.fields/fieldprint/printerinstructions/) { get; set; } | Ruft die druckerspezifischen Steuercodezeichen oder PostScript-Anweisungen ab oder legt diese fest. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ruft Text ab, der zwischen dem Feldtrennzeichen und dem Feldende liegt, oder legt diesen fest. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann sein`Null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl der Feldcode als auch das Feldergebnis der untergeordneten Felder sind enthalten. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). |
| [Remove](../../aspose.words.fields/field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte child seines übergeordneten Knotens ist, wird dessen übergeordneter Absatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben`Null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Führt das Feld unlink aus. |
| [Update](../../aspose.words.fields/field/update/)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

### Bemerkungen

Eine Anweisung zum Senden der druckerspezifischen Steuercodezeichen an den ausgewählten Drucker , wenn das Dokument gedruckt wird.

### Beispiele

Zeigt an, wie ein PRINT-Feld eingefügt werden soll.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("My paragraph");

// Das PRINT-Feld kann Anweisungen an den Drucker senden.
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


