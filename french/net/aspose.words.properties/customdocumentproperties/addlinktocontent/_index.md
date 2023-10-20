---
title: CustomDocumentProperties.AddLinkToContent
linktitle: AddLinkToContent
articleTitle: AddLinkToContent
second_title: Aspose.Words pour .NET
description: CustomDocumentProperties AddLinkToContent méthode. Crée une nouvelle propriété de document personnalisé liée au contenu en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.properties/customdocumentproperties/addlinktocontent/
---
## CustomDocumentProperties.AddLinkToContent method

Crée une nouvelle propriété de document personnalisé liée au contenu.

```csharp
public DocumentProperty AddLinkToContent(string name, string linkSource)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| name | String | Le nom de la propriété. |
| linkSource | String | La source de la propriété. |

### Return_Value

L'objet de propriété nouvellement créé ou`nul` quand le*linkSource* est invalide.

## Exemples

Montre comment lier une propriété de document personnalisée à un signet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("MyBookmark");
builder.Write("Hello world!");
builder.EndBookmark("MyBookmark");

// Lier une nouvelle propriété personnalisée à un signet. La valeur de cette propriété
// sera le contenu du signet auquel il fait référence dans le membre "LinkSource".
CustomDocumentProperties customProperties = doc.CustomDocumentProperties;
DocumentProperty customProperty = customProperties.AddLinkToContent("Bookmark", "MyBookmark");

Assert.AreEqual(true, customProperty.IsLinkToContent);
Assert.AreEqual("MyBookmark", customProperty.LinkSource);
Assert.AreEqual("Hello world!", customProperty.Value);

doc.Save(ArtifactsDir + "DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
```

### Voir également

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* espace de noms [Aspose.Words.Properties](../../../aspose.words.properties/)
* Assemblée [Aspose.Words](../../../)
