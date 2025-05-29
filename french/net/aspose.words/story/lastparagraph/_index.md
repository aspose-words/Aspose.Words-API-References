---
title: Story.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: Aspose.Words pour .NET
description: Accédez au dernier paragraphe de votre histoire sans effort grâce à la propriété Story LastParagraph, améliorant ainsi votre expérience de gestion et d'édition narrative.
type: docs
weight: 20
url: /fr/net/aspose.words/story/lastparagraph/
---
## Story.LastParagraph property

Obtient le dernier paragraphe de l'histoire.

```csharp
public Paragraph LastParagraph { get; }
```

## Exemples

Montre comment déplacer la position du curseur d'un DocumentBuilder vers un nœud spécifié.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// Le générateur de documents dispose d'un curseur, qui agit comme une partie du document
// où le constructeur ajoute de nouveaux nœuds lorsque nous utilisons ses méthodes de construction de documents.
// Ce curseur fonctionne de la même manière que le curseur clignotant de Microsoft Word,
// et il se termine également toujours immédiatement après tout nœud que le constructeur vient d'insérer.
// Pour ajouter du contenu à une autre partie du document,
// nous pouvons déplacer le curseur vers un nœud différent avec la méthode "MoveTo".
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.Runs[0]);
// Le curseur est maintenant devant le nœud vers lequel nous l'avons déplacé.
// L'ajout d'une deuxième exécution l'insérera devant la première exécution.
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// Déplacez le curseur à la fin du document pour continuer à ajouter du texte à la fin comme auparavant.
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

### Voir également

* class [Paragraph](../../paragraph/)
* class [Story](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
