---
title: FieldFormText Class
linktitle: FieldFormText
articleTitle: FieldFormText
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fields.FieldFormText für die nahtlose Implementierung von FORMTEXT-Feldern. Verbessern Sie noch heute die Dokumentenautomatisierung mit leistungsstarken Funktionen!
type: docs
weight: 2340
url: /de/net/aspose.words.fields/fieldformtext/
---
## FieldFormText class

Implementiert das FORMTEXT-Feld.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class FieldFormText : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldFormText](fieldformtext/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Erhält eine[`FieldFormat`](../fieldformat/)Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (das Ergebnis sollte nicht neu berechnet werden). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
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

Fügt ein Formularfeld im Textfeldstil ein.

## Beispiele

Zeigt, wie die Felder FORMCHECKBOX, FORMDROPDOWN und FORMTEXT verarbeitet werden.

```csharp
// Diese Felder sind veraltete Entsprechungen des FormField. Wir können diese Felder mit Aspose.Words lesen, aber nicht erstellen.
// In Microsoft Word können wir diese Felder über das Menü „Legacy Tools“ auf der Registerkarte „Entwickler“ einfügen.
Document doc = new Document(MyDir + "Form fields.docx");

FieldFormCheckBox fieldFormCheckBox = (FieldFormCheckBox)doc.Range.Fields[1];
Assert.AreEqual(" FORMCHECKBOX \u0001", fieldFormCheckBox.GetFieldCode());

FieldFormDropDown fieldFormDropDown = (FieldFormDropDown)doc.Range.Fields[2];
Assert.AreEqual(" FORMDROPDOWN \u0001", fieldFormDropDown.GetFieldCode());

FieldFormText fieldFormText = (FieldFormText)doc.Range.Fields[0];
Assert.AreEqual(" FORMTEXT \u0001", fieldFormText.GetFieldCode());
```

### Siehe auch

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
