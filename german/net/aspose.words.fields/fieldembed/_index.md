---
title: Class FieldEmbed
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fields.FieldEmbed klas. Implementiert das EMBEDFeld.
type: docs
weight: 1700
url: /de/net/aspose.words.fields/fieldembed/
---
## FieldEmbed class

Implementiert das EMBED-Feld.

```csharp
public class FieldEmbed : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldEmbed](fieldembed/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
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

### Beispiele

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

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)


