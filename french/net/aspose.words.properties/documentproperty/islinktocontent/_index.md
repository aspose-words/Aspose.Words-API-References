---
title: DocumentProperty.IsLinkToContent
linktitle: IsLinkToContent
articleTitle: IsLinkToContent
second_title: Aspose.Words pour .NET
description: Découvrez si la propriété IsLinkToContent de DocumentProperty est connectée au contenu. Améliorez votre flux de travail grâce à des solutions de gestion documentaire fluides.
type: docs
weight: 10
url: /fr/net/aspose.words.properties/documentproperty/islinktocontent/
---
## DocumentProperty.IsLinkToContent property

Indique si cette propriété est liée au contenu ou non.

```csharp
public bool IsLinkToContent { get; }
```

## Exemples

Montre comment lier une propriété de document personnalisée à un signet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("MyBookmark");
builder.Write("Hello world!");
builder.EndBookmark("MyBookmark");

// Associer une nouvelle propriété personnalisée à un signet. La valeur de cette propriété
// sera le contenu du signet auquel il fait référence dans le membre « LinkSource ».
CustomDocumentProperties customProperties = doc.CustomDocumentProperties;
DocumentProperty customProperty = customProperties.AddLinkToContent("Bookmark", "MyBookmark");

Assert.AreEqual(true, customProperty.IsLinkToContent);
Assert.AreEqual("MyBookmark", customProperty.LinkSource);
Assert.AreEqual("Hello world!", customProperty.Value);

doc.Save(ArtifactsDir + "DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
```

### Voir également

* class [DocumentProperty](../)
* espace de noms [Aspose.Words.Properties](../../../aspose.words.properties/)
* Assemblée [Aspose.Words](../../../)
