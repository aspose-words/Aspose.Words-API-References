---
title: CustomDocumentProperties.AddLinkToContent
linktitle: AddLinkToContent
articleTitle: AddLinkToContent
second_title: Aspose.Words für .NET
description: Entdecken Sie die AddLinkToContent-Methode von CustomDocumentProperties, um mühelos verknüpfte benutzerdefinierte Dokumenteigenschaften für eine verbesserte Dokumentenverwaltung zu erstellen.
type: docs
weight: 20
url: /de/net/aspose.words.properties/customdocumentproperties/addlinktocontent/
---
## CustomDocumentProperties.AddLinkToContent method

Erstellt eine neue, mit dem Inhalt verknüpfte benutzerdefinierte Dokumenteigenschaft.

```csharp
public DocumentProperty AddLinkToContent(string name, string linkSource)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | String | Der Name der Eigenschaft. |
| linkSource | String | Die Quelle der Eigenschaft. |

### Rückgabewert

Das neu erstellte Eigenschaftsobjekt bzw.`null` wenn die*linkSource* ist ungültig.

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

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* namensraum [Aspose.Words.Properties](../../../aspose.words.properties/)
* Montage [Aspose.Words](../../../)
