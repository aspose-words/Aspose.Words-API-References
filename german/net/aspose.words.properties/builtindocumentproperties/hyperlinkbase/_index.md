---
title: BuiltInDocumentProperties.HyperlinkBase
second_title: Aspose.Words für .NET-API-Referenz
description: BuiltInDocumentProperties eigendom. Gibt die Basiszeichenfolge an die zum Auswerten relativer Hyperlinks in diesem Dokument verwendet wird.
type: docs
weight: 120
url: /de/net/aspose.words.properties/builtindocumentproperties/hyperlinkbase/
---
## BuiltInDocumentProperties.HyperlinkBase property

Gibt die Basiszeichenfolge an, die zum Auswerten relativer Hyperlinks in diesem Dokument verwendet wird.

```csharp
public string HyperlinkBase { get; set; }
```

### Bemerkungen

Aspose.Words verwendet diese Eigenschaft nicht.

### Beispiele

Zeigt, wie der Basisteil eines Hyperlinks in den Eigenschaften des Dokuments gespeichert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Einfügen eines relativen Hyperlinks zu einem Dokument im lokalen Dateisystem mit dem Namen "Document.docx".
// Wenn Sie in Microsoft Word auf den Link klicken, wird das angegebene Dokument geöffnet, sofern verfügbar.
builder.InsertHyperlink("Relative hyperlink", "Document.docx", false);

// Dieser Link ist relativ. Wenn es im selben Ordner kein "Document.docx" gibt
// als das Dokument, das diesen Link enthält, wird der Link unterbrochen.
Assert.False(File.Exists(ArtifactsDir + "Document.docx"));
doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.BrokenLink.docx");

// Das Dokument, auf das wir verlinken möchten, befindet sich in einem anderen Verzeichnis als dem, in dem wir das Dokument speichern möchten.
// Wir könnten solche Links reparieren, indem wir in jeden einen absoluten Dateinamen einfügen. 
// Alternativ könnten wir einen Basislink bereitstellen, der jeden Hyperlink mit einem relativen Dateinamen enthält
// wird seinem Link vorangestellt, wenn wir darauf klicken. 
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;
properties.HyperlinkBase = MyDir;

Assert.True(File.Exists(properties.HyperlinkBase + ((FieldHyperlink)doc.Range.Fields[0]).Address));

doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.WorkingLink.docx");
```

### Siehe auch

* class [BuiltInDocumentProperties](../)
* namensraum [Aspose.Words.Properties](../../builtindocumentproperties/)
* Montage [Aspose.Words](../../../)


