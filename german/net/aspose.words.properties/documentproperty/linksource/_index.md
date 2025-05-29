---
title: DocumentProperty.LinkSource
linktitle: LinkSource
articleTitle: LinkSource
second_title: Aspose.Words für .NET
description: Entdecken Sie die LinkSource-Eigenschaft für DocumentProperty und greifen Sie mühelos auf die Quelle Ihrer verknüpften benutzerdefinierten Dokumenteigenschaften zu, um die Dokumentenverwaltung zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words.properties/documentproperty/linksource/
---
## DocumentProperty.LinkSource property

Ruft die Quelle einer verknüpften benutzerdefinierten Dokumenteigenschaft ab.

```csharp
public string LinkSource { get; }
```

## Beispiele

Zeigt, wie eine benutzerdefinierte Dokumenteigenschaft mit einem Lesezeichen verknüpft wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("MyBookmark");
builder.Write("Hello world!");
builder.EndBookmark("MyBookmark");

// Verknüpfen Sie eine neue benutzerdefinierte Eigenschaft mit einem Lesezeichen. Der Wert dieser Eigenschaft
// wird der Inhalt des Lesezeichens sein, auf das im Mitglied „LinkSource“ verwiesen wird.
CustomDocumentProperties customProperties = doc.CustomDocumentProperties;
DocumentProperty customProperty = customProperties.AddLinkToContent("Bookmark", "MyBookmark");

Assert.AreEqual(true, customProperty.IsLinkToContent);
Assert.AreEqual("MyBookmark", customProperty.LinkSource);
Assert.AreEqual("Hello world!", customProperty.Value);

doc.Save(ArtifactsDir + "DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
```

### Siehe auch

* class [DocumentProperty](../)
* namensraum [Aspose.Words.Properties](../../../aspose.words.properties/)
* Montage [Aspose.Words](../../../)
