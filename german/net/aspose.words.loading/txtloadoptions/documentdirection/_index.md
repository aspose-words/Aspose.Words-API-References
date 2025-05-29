---
title: TxtLoadOptions.DocumentDirection
linktitle: DocumentDirection
articleTitle: DocumentDirection
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „DocumentDirection“ von TxtLoadOptions, um die Dokumentrichtung einfach festzulegen. Optimieren Sie Ihr Layout mit der Standardeinstellung „LeftToRight“!
type: docs
weight: 50
url: /de/net/aspose.words.loading/txtloadoptions/documentdirection/
---
## TxtLoadOptions.DocumentDirection property

Ruft eine Dokumentrichtung ab oder legt sie fest. Der Standardwert istLeftToRight .

```csharp
public DocumentDirection DocumentDirection { get; set; }
```

## Beispiele

Zeigt, wie die Textrichtung in Klartextdokumenten erkannt wird.

```csharp
// Erstelle ein "TxtLoadOptions"-Objekt, das wir an den Konstruktor eines Dokuments übergeben können
// um zu ändern, wie wir ein Klartextdokument laden.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Setzen Sie die Eigenschaft "DocumentDirection" auf "DocumentDirection.Auto" erkennt automatisch
// die Richtung jedes Textabsatzes, den Aspose.Words aus dem Klartext lädt.
// Die „Bidi“-Eigenschaft jedes Absatzes speichert seine Richtung.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// Hebräischen Text als von rechts nach links lesend erkennen.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// Englischen Text als von rechts nach links lesend erkennen.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

### Siehe auch

* enum [DocumentDirection](../../documentdirection/)
* class [TxtLoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
