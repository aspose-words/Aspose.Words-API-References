---
title: DocumentProperty.LinkSource
linktitle: LinkSource
articleTitle: LinkSource
second_title: Aspose.Words pour .NET
description: Découvrez la propriété LinkSource pour DocumentProperty, accédez sans effort à la source de vos propriétés de document personnalisées liées pour une gestion améliorée des documents.
type: docs
weight: 20
url: /fr/net/aspose.words.properties/documentproperty/linksource/
---
## DocumentProperty.LinkSource property

Obtient la source d'une propriété de document personnalisé liée.

```csharp
public string LinkSource { get; }
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
