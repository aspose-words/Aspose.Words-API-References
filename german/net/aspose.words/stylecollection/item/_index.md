---
title: StyleCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words für .NET
description: Entdecken Sie die leistungsstarke Item-Eigenschaft von StyleCollection, um mühelos Stile nach Namen oder Alias abzurufen und so Ihr Designerlebnis mühelos zu verbessern!
type: docs
weight: 50
url: /de/net/aspose.words/stylecollection/item/
---
## StyleCollection indexer (1 of 3)

Ruft einen Stil nach Name oder Alias ab.

```csharp
public Style this[string name] { get; }
```

## Bemerkungen

Groß- und Kleinschreibung beachten, Rückgaben`null` wenn der Stil mit dem angegebenen Namen nicht gefunden wird.

Wenn es sich um den englischen Namen eines integrierten Stils handelt, der noch nicht vorhanden ist, wird dieser automatisch erstellt.

## Beispiele

Zeigt an, wann das Seitenlayout des Dokuments neu berechnet werden muss.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Das Speichern eines Dokuments als PDF, als Bild oder beim ersten Drucken wird automatisch
// Cachen Sie das Layout des Dokuments innerhalb seiner Seiten.
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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## StyleCollection indexer (2 of 3)

Ruft einen integrierten Stil über seine lokal unabhängige Kennung ab.

```csharp
public Style this[StyleIdentifier sti] { get; }
```

| Parameter | Beschreibung |
| --- | --- |
| sti | A[`StyleIdentifier`](../../styleidentifier/) Wert, der den abzurufenden integrierten Stil angibt. |

## Bemerkungen

Beim Zugriff auf einen Stil, der noch nicht existiert, wird dieser automatisch erstellt.

## Beispiele

Zeigt, wie der Stilsammlung eines Dokuments ein Stil hinzugefügt wird.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Legen Sie Standardparameter für neue Stile fest, die wir dieser Sammlung später hinzufügen können.
styles.DefaultFont.Name = "Courier New";
// Wenn wir einen Stil vom Typ "StyleType.Paragraph" hinzufügen, wendet die Sammlung die Werte von
// seine Eigenschaft „DefaultParagraphFormat“ zur Eigenschaft „ParagraphFormat“ des Stils.
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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## StyleCollection indexer (3 of 3)

Ruft einen Stil nach Index ab.

```csharp
public Style this[int index] { get; }
```

## Beispiele

Zeigt, wie der Stilsammlung eines Dokuments ein Stil hinzugefügt wird.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Legen Sie Standardparameter für neue Stile fest, die wir dieser Sammlung später hinzufügen können.
styles.DefaultFont.Name = "Courier New";
// Wenn wir einen Stil vom Typ "StyleType.Paragraph" hinzufügen, wendet die Sammlung die Werte von
// seine Eigenschaft „DefaultParagraphFormat“ zur Eigenschaft „ParagraphFormat“ des Stils.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// Fügen Sie einen Stil hinzu und überprüfen Sie dann, ob er die Standardeinstellungen hat.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### Siehe auch

* class [Style](../../style/)
* class [StyleCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
