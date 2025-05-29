---
title: BuiltInDocumentProperties.HyperlinkBase
linktitle: HyperlinkBase
articleTitle: HyperlinkBase
second_title: Aspose.Words für .NET
description: Entdecken Sie die HyperlinkBase-Eigenschaft von BuiltInDocumentProperties, um relative Hyperlinks in Ihren Dokumenten für eine nahtlose Navigation und ein verbessertes Benutzererlebnis zu optimieren.
type: docs
weight: 120
url: /de/net/aspose.words.properties/builtindocumentproperties/hyperlinkbase/
---
## BuiltInDocumentProperties.HyperlinkBase property

Gibt die Basiszeichenfolge an, die zur Auswertung relativer Hyperlinks in diesem Dokument verwendet wird.

```csharp
public string HyperlinkBase { get; set; }
```

## Bemerkungen

Aspose.Words verwendet diese Eigenschaft nicht.

## Beispiele

Zeigt, wie der Basisteil eines Hyperlinks in den Eigenschaften des Dokuments gespeichert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie einen relativen Hyperlink zu einem Dokument im lokalen Dateisystem mit dem Namen „Document.docx“ ein.
// Durch Klicken auf den Link in Microsoft Word wird das gewünschte Dokument geöffnet, sofern es verfügbar ist.
builder.InsertHyperlink("Relative hyperlink", "Document.docx", false);

// Dieser Link ist relativ. Wenn im selben Ordner kein "Document.docx" vorhanden ist
// Da das Dokument diesen Link enthält, wird der Link unterbrochen.
Assert.False(File.Exists(ArtifactsDir + "Document.docx"));
doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.BrokenLink.docx");

// Das Dokument, auf das wir eine Verknüpfung herstellen möchten, befindet sich in einem anderen Verzeichnis als dem, in dem wir das Dokument speichern möchten.
    // Wir könnten solche Links reparieren, indem wir in jeden einen absoluten Dateinamen einfügen.
// Alternativ könnten wir einen Basislink bereitstellen, der jeden Hyperlink mit einem relativen Dateinamen
    // wird seinem Link vorangestellt, wenn wir darauf klicken.
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;
properties.HyperlinkBase = MyDir;

Assert.True(File.Exists(properties.HyperlinkBase + ((FieldHyperlink)doc.Range.Fields[0]).Address));

doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.WorkingLink.docx");
```

### Siehe auch

* class [BuiltInDocumentProperties](../)
* namensraum [Aspose.Words.Properties](../../../aspose.words.properties/)
* Montage [Aspose.Words](../../../)
