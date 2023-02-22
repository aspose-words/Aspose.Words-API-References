---
title: ParagraphFormat.SuppressAutoHyphens
second_title: Aspose.Words für .NET-API-Referenz
description: ParagraphFormat eigendom. Gibt an ob der aktuelle Absatz von jeglicher Silbentrennung ausgenommen werden soll die in den Dokumenteinstellungen angewendet wird.
type: docs
weight: 360
url: /de/net/aspose.words/paragraphformat/suppressautohyphens/
---
## ParagraphFormat.SuppressAutoHyphens property

Gibt an, ob der aktuelle Absatz von jeglicher Silbentrennung ausgenommen werden soll, die in den Dokumenteinstellungen angewendet wird.

```csharp
public bool SuppressAutoHyphens { get; set; }
```

### Beispiele

Zeigt, wie die Silbentrennung für einen Absatz unterdrückt wird.

```csharp
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Öffnen Sie ein Dokument, das Text enthält, dessen Gebietsschema mit dem unseres Wörterbuchs übereinstimmt.
// Wenn wir dieses Dokument in einem festen Seitenspeicherformat speichern, wird sein Text getrennt.
Document doc = new Document(MyDir + "German text.docx");

// Wir können die Eigenschaft "SuppressAutoHyphens" auf "true" setzen, um die Silbentrennung zu deaktivieren
// für einen bestimmten Absatz, während es für den Rest des Dokuments aktiviert bleibt.
// Der Standardwert für diese Eigenschaft ist "false",
// was bedeutet, dass jeder Absatz standardmäßig eine Silbentrennung verwendet, falls vorhanden.
doc.FirstSection.Body.FirstParagraph.ParagraphFormat.SuppressAutoHyphens = suppressAutoHyphens;

doc.Save(ArtifactsDir + "ParagraphFormat.SuppressHyphens.pdf");
```

### Siehe auch

* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../paragraphformat/)
* Montage [Aspose.Words](../../../)


