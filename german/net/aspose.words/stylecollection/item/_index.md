---
title: StyleCollection.Item
second_title: Aspose.Words für .NET-API-Referenz
description: StyleCollection eigendom. Ruft einen Stil nach Namen oder Alias ab.
type: docs
weight: 50
url: /de/net/aspose.words/stylecollection/item/
---
## StyleCollection indexer (1 of 3)

Ruft einen Stil nach Namen oder Alias ab.

```csharp
public Style this[string name] { get; }
```

### Bemerkungen

Groß- und Kleinschreibung beachten, Rückgaben`Null` wenn der Stil mit dem angegebenen Namen nicht gefunden wird.

Wenn es sich um einen englischen Namen eines integrierten Stils handelt, der noch nicht existiert, wird er automatisch erstellt.

### Beispiele

Zeigt an, wann das Seitenlayout des Dokuments neu berechnet werden soll.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Das Speichern eines Dokuments als PDF, ein Bild oder das erstmalige Drucken erfolgt automatisch
// Das Layout des Dokuments innerhalb seiner Seiten zwischenspeichern.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Das Dokument auf irgendeine Weise ändern.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

 // In der aktuellen Version von Aspose.Words wird das Dokument beim Ändern nicht automatisch neu erstellt
// das zwischengespeicherte Seitenlayout. Wenn wir das zwischengespeicherte Layout wünschen
// Um auf dem neuesten Stand zu bleiben, müssen wir es manuell aktualisieren.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### Siehe auch

* class [Style](../../style/)
* class [StyleCollection](../)
* namensraum [Aspose.Words](../../stylecollection/)
* Montage [Aspose.Words](../../../)

---

## StyleCollection indexer (2 of 3)

Ruft einen integrierten Stil anhand seiner vom Gebietsschema unabhängigen Kennung ab.

```csharp
public Style this[StyleIdentifier sti] { get; }
```

| Parameter | Beschreibung |
| --- | --- |
| sti | A[`StyleIdentifier`](../../styleidentifier/) Wert, der den integrierten Stil angibt, der abgerufen werden soll. |

### Bemerkungen

Beim Zugriff auf einen Stil, der noch nicht existiert, wird dieser automatisch erstellt.

### Beispiele

Zeigt, wie man der Stilsammlung eines Dokuments einen Stil hinzufügt.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Standardparameter für neue Stile festlegen, die wir später möglicherweise zu dieser Sammlung hinzufügen.
styles.DefaultFont.Name = "Courier New";
// Wenn wir einen Stil von „StyleType.Paragraph“ hinzufügen, wendet die Sammlung die Werte von an
// seine „DefaultParagraphFormat“-Eigenschaft zur „ParagraphFormat“-Eigenschaft des Stils.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// Fügen Sie einen Stil hinzu und überprüfen Sie dann, ob er die Standardeinstellungen hat.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### Siehe auch

* class [Style](../../style/)
* enum [StyleIdentifier](../../styleidentifier/)
* class [StyleCollection](../)
* namensraum [Aspose.Words](../../stylecollection/)
* Montage [Aspose.Words](../../../)

---

## StyleCollection indexer (3 of 3)

Ruft einen Stil nach Index ab.

```csharp
public Style this[int index] { get; }
```

### Beispiele

Zeigt, wie man der Stilsammlung eines Dokuments einen Stil hinzufügt.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Standardparameter für neue Stile festlegen, die wir später möglicherweise zu dieser Sammlung hinzufügen.
styles.DefaultFont.Name = "Courier New";
// Wenn wir einen Stil von „StyleType.Paragraph“ hinzufügen, wendet die Sammlung die Werte von an
// seine „DefaultParagraphFormat“-Eigenschaft zur „ParagraphFormat“-Eigenschaft des Stils.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// Fügen Sie einen Stil hinzu und überprüfen Sie dann, ob er die Standardeinstellungen hat.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### Siehe auch

* class [Style](../../style/)
* class [StyleCollection](../)
* namensraum [Aspose.Words](../../stylecollection/)
* Montage [Aspose.Words](../../../)


