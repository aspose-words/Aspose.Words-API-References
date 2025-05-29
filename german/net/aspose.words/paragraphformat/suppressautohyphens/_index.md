---
title: ParagraphFormat.SuppressAutoHyphens
linktitle: SuppressAutoHyphens
articleTitle: SuppressAutoHyphens
second_title: Aspose.Words für .NET
description: Steuern Sie die Silbentrennung in Ihrem Dokument mit der Eigenschaft „SuppressAutoHyphens“ von ParagraphFormat und sorgen Sie so für eine klare und professionelle Absatzformatierung.
type: docs
weight: 380
url: /de/net/aspose.words/paragraphformat/suppressautohyphens/
---
## ParagraphFormat.SuppressAutoHyphens property

Gibt an, ob der aktuelle Absatz von der Silbentrennung ausgenommen werden soll, die in den Dokumenteinstellungen angewendet wird.

```csharp
public bool SuppressAutoHyphens { get; set; }
```

## Beispiele

Zeigt, wie die Silbentrennung für einen Absatz unterdrückt wird.

```csharp
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Öffnen Sie ein Dokument mit Text, dessen Gebietsschema mit dem unseres Wörterbuchs übereinstimmt.
// Wenn wir dieses Dokument in einem festen Seitenspeicherformat speichern, wird der Text getrennt.
Document doc = new Document(MyDir + "German text.docx");

// Wir können die Eigenschaft "SuppressAutoHyphens" auf "true" setzen, um die Silbentrennung zu deaktivieren
// für einen bestimmten Absatz, während es für den Rest des Dokuments aktiviert bleibt.
// Der Standardwert für diese Eigenschaft ist „false“,
// was bedeutet, dass in jedem Absatz standardmäßig die Silbentrennung verwendet wird, sofern eine solche verfügbar ist.
doc.FirstSection.Body.FirstParagraph.ParagraphFormat.SuppressAutoHyphens = suppressAutoHyphens;

doc.Save(ArtifactsDir + "ParagraphFormat.SuppressHyphens.pdf");
```

### Siehe auch

* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
