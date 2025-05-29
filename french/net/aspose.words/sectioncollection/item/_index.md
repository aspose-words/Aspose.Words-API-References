---
title: SectionCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words pour .NET
description: Accédez facilement à des sections spécifiques grâce à la propriété SectionCollection Item. Récupérez n'importe quelle section par index pour une gestion simplifiée des données.
type: docs
weight: 10
url: /fr/net/aspose.words/sectioncollection/item/
---
## SectionCollection indexer

Récupère une section à l'index donné.

```csharp
public Section this[int index] { get; }
```

| Paramètre | La description |
| --- | --- |
| index | Un index dans la liste des sections. |

## Remarques

L'indice est basé sur zéro.

Les index négatifs sont autorisés et indiquent l'accès depuis l'arrière de la collection. Par exemple, -1 signifie le dernier élément, -2 signifie l'avant-dernier et ainsi de suite.

Si l'index est supérieur ou égal au nombre d'éléments dans la liste, cela renvoie une référence nulle.

Si l'index est négatif et que sa valeur absolue est supérieure au nombre d'éléments dans la liste, cela renvoie une référence nulle.

## Exemples

Indique quand recalculer la mise en page du document.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// L'enregistrement d'un document au format PDF, dans une image ou l'impression pour la première fois sera automatiquement
// mettre en cache la mise en page du document dans ses pages.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Modifier le document d'une manière ou d'une autre.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

// Dans la version actuelle d'Aspose.Words, la modification du document ne le reconstruit pas automatiquement
// la mise en page en cache. Si nous souhaitons la mise en page en cache
// pour rester à jour, nous devrons le mettre à jour manuellement.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

Montre comment préparer un nouveau nœud de section pour l'édition.

```csharp
Document doc = new Document();

// Un document vierge est livré avec une section, qui a un corps, qui à son tour a un paragraphe.
// Nous pouvons ajouter du contenu à ce document en ajoutant des éléments tels que des passages de texte, des formes ou des tableaux à ce paragraphe.
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// Si nous ajoutons une nouvelle section comme celle-ci, elle n'aura pas de corps, ni aucun autre nœud enfant.
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// Exécutez la méthode « EnsureMinimum » pour ajouter un corps et un paragraphe à cette section pour commencer à la modifier.
doc.LastSection.EnsureMinimum();

Assert.AreEqual(NodeType.Body, doc.Sections[1].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[1].Body.GetChild(NodeType.Any, 0, true).NodeType);

doc.Sections[0].Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Voir également

* class [Section](../../section/)
* class [SectionCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
