---
title: FieldFileSize Class
linktitle: FieldFileSize
articleTitle: FieldFileSize
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fields.FieldFileSize zur mühelosen Implementierung des Felds FILESIZE und verbessern Sie so problemlos die Dokumentenverwaltung.
type: docs
weight: 2290
url: /de/net/aspose.words.fields/fieldfilesize/
---
## FieldFileSize class

Implementiert das Feld FILESIZE.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class FieldFileSize : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldFileSize](fieldfilesize/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Erhält eine[`FieldFormat`](../fieldformat/)Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsInKilobytes](../../aspose.words.fields/fieldfilesize/isinkilobytes/) { get; set; } | Ruft ab oder legt fest, ob die Dateigröße in Kilobyte angezeigt werden soll. |
| [IsInMegabytes](../../aspose.words.fields/fieldfilesize/isinmegabytes/) { get; set; } | Ruft ab oder legt fest, ob die Dateigröße in Megabyte angezeigt werden soll. |
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

Ruft die Größe der Datei des aktuellen Dokuments ab oder 0, wenn die Größe nicht bestimmt werden kann.

In der aktuellen Implementierung verwendet die[`OriginalFileName`](../../aspose.words/document/originalfilename/) Eigenschaft zum Abrufen des Dateinamens, der zum Bestimmen der Dateigröße verwendet wird.

## Beispiele

Zeigt, wie die Dateigröße eines Dokuments mit einem FILESIZE-Feld angezeigt wird.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(18105, doc.BuiltInDocumentProperties.Bytes);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertParagraph();

// Unten sind drei verschiedene Maßeinheiten
// mit denen FILESIZE-Felder die Dateigröße des Dokuments anzeigen können.
// 1 - Bytes:
FieldFileSize field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.Update();

Assert.AreEqual(" FILESIZE ", field.GetFieldCode());
Assert.AreEqual("18105", field.Result);

// 2 - Kilobyte:
builder.InsertParagraph();
field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.IsInKilobytes = true;
field.Update();

Assert.AreEqual(" FILESIZE  \\k", field.GetFieldCode());
Assert.AreEqual("18", field.Result);

// 3 - Megabyte:
builder.InsertParagraph();
field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.IsInMegabytes = true;
field.Update();

Assert.AreEqual(" FILESIZE  \\m", field.GetFieldCode());
Assert.AreEqual("0", field.Result);

// Um die Werte dieser Felder während der Bearbeitung in Microsoft Word zu aktualisieren,
// Wir müssen zuerst die Änderungen speichern und diese Felder dann manuell aktualisieren.
doc.Save(ArtifactsDir + "Field.FILESIZE.docx");
```

### Siehe auch

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
