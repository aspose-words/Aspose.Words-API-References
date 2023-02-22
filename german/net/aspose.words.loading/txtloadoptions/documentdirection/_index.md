---
title: TxtLoadOptions.DocumentDirection
second_title: Aspose.Words für .NET-API-Referenz
description: TxtLoadOptions eigendom. Ruft eine Dokumentrichtung ab oder legt sie fest. Der Standardwert istLeftToRight .
type: docs
weight: 30
url: /de/net/aspose.words.loading/txtloadoptions/documentdirection/
---
## TxtLoadOptions.DocumentDirection property

Ruft eine Dokumentrichtung ab oder legt sie fest. Der Standardwert istLeftToRight .

```csharp
public DocumentDirection DocumentDirection { get; set; }
```

### Beispiele

Zeigt, wie die Textrichtung von Klartextdokumenten erkannt wird.

```csharp
// Erstellen Sie ein "TxtLoadOptions"-Objekt, das wir an den Konstruktor eines Dokuments übergeben können
// um zu ändern, wie wir ein Klartextdokument laden.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Setzen Sie die Eigenschaft "DocumentDirection" auf "DocumentDirection.Auto" wird automatisch erkannt
// die Richtung jedes Textabsatzes, den Aspose.Words aus Klartext lädt.
// Die "Bidi"-Eigenschaft jedes Absatzes speichert seine Richtung.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// Hebräischen Text von rechts nach links erkennen.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// Englischen Text von rechts nach links erkennen.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

### Siehe auch

* enum [DocumentDirection](../../documentdirection/)
* class [TxtLoadOptions](../)
* namensraum [Aspose.Words.Loading](../../txtloadoptions/)
* Montage [Aspose.Words](../../../)


