---
title: Paragraph.GetText
linktitle: GetText
articleTitle: GetText
second_title: Aspose.Words pour .NET
description: Découvrez la méthode Paragraph GetText pour récupérer sans effort du texte, y compris les fins de paragraphe, améliorant ainsi l'efficacité de votre traitement de texte.
type: docs
weight: 280
url: /fr/net/aspose.words/paragraph/gettext/
---
## Paragraph.GetText method

Obtient le texte de ce paragraphe, y compris le caractère de fin de paragraphe.

```csharp
public override string GetText()
```

## Remarques

Le texte de tous les nœuds enfants est concaténé et le caractère de fin de paragraphe est ajouté comme suit :

* Si le paragraphe est le dernier paragraphe de[`Body`](../../body/) , alors [`SectionBreak`](../../controlchar/sectionbreak/) (\x000c) est ajouté.
* Si le paragraphe est le dernier paragraphe de[`Cell`](../../../aspose.words.tables/cell/) , alors [`Cell`](../../controlchar/cell/) (\x0007) est ajouté.
* Pour tous les autres paragraphes [`ParagraphBreak`](../../controlchar/paragraphbreak/) (\r) est ajouté.

La chaîne renvoyée inclut tous les caractères de contrôle et spéciaux comme décrit dans[`ControlChar`](../../controlchar/).

## Exemples

Montre comment ajouter, mettre à jour et supprimer des nœuds enfants dans la collection d'enfants d'un CompositeNode.

```csharp
Document doc = new Document();

// Un document vide, par défaut, comporte un paragraphe.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Les nœuds composites tels que notre paragraphe peuvent contenir d'autres nœuds composites et en ligne comme enfants.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Créez trois nœuds d'exécution supplémentaires.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// Le corps du document n'affichera pas ces exécutions tant que nous ne les aurons pas insérées dans un nœud composite
// qui fait lui-même partie de l'arborescence des nœuds du document, comme nous l'avons fait lors de la première exécution.
// Nous pouvons déterminer où se trouve le contenu textuel des nœuds que nous insérons
// apparaît dans le document en spécifiant un emplacement d'insertion par rapport à un autre nœud du paragraphe.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// Insérer la deuxième exécution dans le paragraphe devant l'exécution initiale.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// Insérer la troisième exécution après l'exécution initiale.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// Insérer la première exécution au début de la collection de nœuds enfants du paragraphe.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// Nous pouvons modifier le contenu de l'exécution en modifiant et en supprimant les nœuds enfants existants.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### Voir également

* class [Paragraph](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
