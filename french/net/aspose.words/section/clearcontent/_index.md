---
title: Section.ClearContent
second_title: Référence de l'API Aspose.Words pour .NET
description: Section méthode. Efface la section.
type: docs
weight: 110
url: /fr/net/aspose.words/section/clearcontent/
---
## Section.ClearContent method

Efface la section.

```csharp
public void ClearContent()
```

### Remarques

Le texte de[`Body`](../body/) est effacé, il ne reste qu'un seul paragraphe vide qui représente le saut de section.

Le texte de tous les en-têtes et pieds de page est effacé, mais[`HeaderFooter`](../../headerfooter/) les objets eux-mêmes ne sont pas supprimés.

### Exemples

Montre comment effacer le contenu d’une section.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.GetText().Trim());
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// L'exécution de la méthode "ClearContent" supprimera tout le contenu de la section
// mais laisse un paragraphe vide pour ajouter à nouveau du contenu.
doc.FirstSection.ClearContent();

Assert.AreEqual(string.Empty, doc.GetText().Trim());
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);
```

### Voir également

* class [Section](../)
* espace de noms [Aspose.Words](../../section/)
* Assemblée [Aspose.Words](../../../)


