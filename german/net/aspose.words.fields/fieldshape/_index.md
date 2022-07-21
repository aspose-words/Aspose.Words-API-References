---
title: FieldShape
second_title: Aspose.Words für .NET-API-Referenz
description: Implementiert das SHAPE-Feld.
type: docs
weight: 2260
url: /de/net/aspose.words.fields/fieldshape/
---
## FieldShape class

Implementiert das SHAPE-Feld.

```csharp
public class FieldShape : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldShape](fieldshape)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format) { get; } | erhält a[`FieldFormat`](../fieldformat) Objekt, das typisierten Zugriff auf die Feldformatierung bereitstellt. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Liest oder setzt Text, der zwischen dem Feldtrennzeichen und dem Feldende steht. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann null sein. |
| [Start](../../aspose.words.fields/field/start) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| [Text](../../aspose.words.fields/fieldshape/text) { get; set; } | Ruft den abzurufenden Text ab oder legt ihn fest. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

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

Ruft den angegebenen Text ab.

### Beispiele

Zeigt, wie von rechts nach links kompatible Listen mit BIDIOUTLINE-Feldern erstellt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Das Feld BIDIOUTLINE nummeriert Absätze wie die Felder AUTONUM/LISTNUM,
// ist aber nur sichtbar, wenn eine Rechts-nach-links-Bearbeitungssprache aktiviert ist, z. B. Hebräisch oder Arabisch.
// Das folgende Feld zeigt ".1" an, das RTL-Äquivalent der Listennummer "1.".
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// Fügen Sie zwei weitere BIDIOUTLINE-Felder hinzu, die ".2" und ".3" anzeigen.
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// Legen Sie die horizontale Textausrichtung für jeden Absatz im Dokument auf RTL fest.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// Wenn wir in Microsoft Word eine Bearbeitungssprache von rechts nach links aktivieren, zeigen unsere Felder Zahlen an.
// Andernfalls wird "###" angezeigt.
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

Zeigt, wie einige ältere Microsoft Word-Felder wie SHAPE und EMBED beim Laden behandelt werden.

```csharp
// Öffnen Sie ein Dokument, das in Microsoft Word 2003 erstellt wurde.
Document doc = new Document(MyDir + "Legacy fields.doc");

// Wenn wir das Word-Dokument öffnen und Alt+F9 drücken, sehen wir ein SHAPE- und ein EMBED-Feld.
// Ein SHAPE-Feld ist der Anker/Leinwand für ein AutoShape-Objekt mit aktiviertem Umbruchstil "In Linie mit Text".
// Ein EMBED-Feld hat die gleiche Funktion, aber für ein eingebettetes Objekt
// wie eine Tabelle aus einem externen Excel-Dokument.
// Diese Felder werden jedoch nicht in der Fields-Sammlung des Dokuments angezeigt.
Assert.AreEqual(0, doc.Range.Fields.Count);

// Diese Felder werden nur von alten Versionen von Microsoft Word unterstützt.
// Der Dokumentladeprozess konvertiert diese Felder in Shape-Objekte,
// auf die wir in der Knotensammlung des Dokuments zugreifen können.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
Assert.AreEqual(3, shapes.Count);

// Der erste Shape-Knoten entspricht dem SHAPE-Feld im Eingabedokument,
// Dies ist die Inline-Leinwand für die AutoForm.
Shape shape = (Shape)shapes[0];
Assert.AreEqual(ShapeType.Image, shape.ShapeType);

// Der zweite Shape-Knoten ist die AutoForm selbst.
shape = (Shape)shapes[1];
Assert.AreEqual(ShapeType.Can, shape.ShapeType);

// Die dritte Form ist das Feld EMBED, das die externe Tabelle enthielt.
shape = (Shape)shapes[2];
Assert.AreEqual(ShapeType.OleObject, shape.ShapeType);
```

### Siehe auch

* class [Field](../field)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
