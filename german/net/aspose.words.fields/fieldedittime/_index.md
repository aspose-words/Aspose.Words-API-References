---
title: FieldEditTime Class
linktitle: FieldEditTime
articleTitle: FieldEditTime
second_title: Aspose.Words für .NET
description: Aspose.Words.Fields.FieldEditTime klas. Implementiert das EDITTIMEFeld in C#.
type: docs
weight: 1840
url: /de/net/aspose.words.fields/fieldedittime/
---
## FieldEditTime class

Implementiert das EDITTIME-Feld.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class FieldEditTime : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldEditTime](fieldedittime/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Ruft a ab[`FieldFormat`](../fieldformat/) Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ruft Text ab, der zwischen dem Feldtrennzeichen und dem Feldende liegt, oder legt diesen fest. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann sein`Null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl der Feldcode als auch das Feldergebnis der untergeordneten Felder sind enthalten. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). |
| [Remove](../../aspose.words.fields/field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte child seines übergeordneten Knotens ist, wird dessen übergeordneter Absatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben`Null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Führt das Feld unlink aus. |
| [Update](../../aspose.words.fields/field/update/)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

## Bemerkungen

Ruft die gesamte Bearbeitungszeit in Minuten ab, seit das Dokument erstellt wurde.

## Beispiele

Zeigt, wie das EDITTIME-Feld verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Das EDITTIME-Feld zeigt in Minuten an:
// die Zeit, die mit dem Öffnen des Dokuments in einem Microsoft Word-Fenster verbracht wurde.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("You've been editing this document for ");
FieldEditTime field = (FieldEditTime)builder.InsertField(FieldType.FieldEditTime, true);
builder.Writeln(" minutes.");

// Diese integrierte Dokumenteigenschaft verfolgt die Minuten. Microsoft Word verwendet diese Eigenschaft
// um die Zeit zu verfolgen, die mit dem Öffnen des Dokuments verbracht wurde. Wir können es auch selbst bearbeiten.
doc.BuiltInDocumentProperties.TotalEditingTime = 10;
field.Update();

Assert.AreEqual(" EDITTIME ", field.GetFieldCode());
Assert.AreEqual("10", field.Result);

// Das Feld aktualisiert sich nicht in Echtzeit und muss dies auch tun
// manuell in Microsoft Word aktualisiert, wann immer wir einen genauen Wert benötigen.
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.EDITTIME.docx");
```

### Siehe auch

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
