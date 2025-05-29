---
title: DocumentProperty.IsLinkToContent
linktitle: IsLinkToContent
articleTitle: IsLinkToContent
second_title: Aspose.Words für .NET
description: Ermitteln Sie, ob die Eigenschaft „IsLinkToContent“ von DocumentProperty eine Verbindung zum Inhalt herstellt. Verbessern Sie Ihren Workflow mit nahtlosen Dokumentenmanagementlösungen.
type: docs
weight: 10
url: /de/net/aspose.words.properties/documentproperty/islinktocontent/
---
## DocumentProperty.IsLinkToContent property

Zeigt an, ob diese Eigenschaft mit Inhalt verknüpft ist oder nicht.

```csharp
public bool IsLinkToContent { get; }
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
