---
title: FieldAuthor
second_title: Aspose.Words für .NET-API-Referenz
description: Implementiert das AUTHORFeld.
type: docs
weight: 1420
url: /de/net/aspose.words.fields/fieldauthor/
---
## FieldAuthor class

Implementiert das AUTHOR-Feld.

```csharp
public class FieldAuthor : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldAuthor](fieldauthor/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AuthorName](../../aspose.words.fields/fieldauthor/authorname/) { get; set; } | Ruft den Namen des Dokumentautors ab oder legt ihn fest. |
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

Ruft den Namen des Dokumentautors ab und legt ihn optional fest, wie in der aufgezeichnet **Autor**Eigenschaft der in integrierten Dokumenteigenschaften.

### Beispiele

Zeigt, wie ein AUTHOR-Feld verwendet wird, um den Namen eines Dokumenterstellers anzuzeigen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// AUTHOR-Felder beziehen ihre Ergebnisse aus der integrierten Dokumenteigenschaft namens "Author".
// Wenn wir ein Dokument in Microsoft Word erstellen und speichern,
// es wird unseren Benutzernamen in dieser Eigenschaft haben.
// Wenn wir jedoch ein Dokument programmgesteuert mit Aspose.Words erstellen,
 // Die Eigenschaft "Autor" ist standardmäßig ein leerer String.
Assert.AreEqual(string.Empty, doc.BuiltInDocumentProperties.Author);

// Legen Sie einen Backup-Autorennamen für die zu verwendenden AUTHOR-Felder fest
// wenn die Eigenschaft "Autor" einen leeren String enthält.
doc.FieldOptions.DefaultDocumentAuthor = "Joe Bloggs";

builder.Write("This document was created by ");
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("Joe Bloggs", field.Result);

// Aktualisieren eines AUTHOR-Felds, das einen Wert enthält
// wendet diesen Wert auf die eingebaute Eigenschaft "Autor" an.
Assert.AreEqual("Joe Bloggs", doc.BuiltInDocumentProperties.Author);

// Wenn Sie diese Eigenschaft ändern und dann das AUTHOR-Feld aktualisieren, wird dieser Wert auf das Feld angewendet.
doc.BuiltInDocumentProperties.Author = "John Doe";      
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("John Doe", field.Result);

// Wenn wir ein AUTHOR-Feld aktualisieren, nachdem wir seine "Name"-Eigenschaft geändert haben,
// dann zeigt das Feld den neuen Namen an und wendet den neuen Namen auf die eingebaute Eigenschaft an.
field.AuthorName = "Jane Doe";
field.Update();

Assert.AreEqual(" AUTHOR  \"Jane Doe\"", field.GetFieldCode());
Assert.AreEqual("Jane Doe", field.Result);

// AUTHOR-Felder wirken sich nicht auf die DefaultDocumentAuthor-Eigenschaft aus.
Assert.AreEqual("Jane Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Joe Bloggs", doc.FieldOptions.DefaultDocumentAuthor);

doc.Save(ArtifactsDir + "Field.AUTHOR.docx");
```

### Siehe auch

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
