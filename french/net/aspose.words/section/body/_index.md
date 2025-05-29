---
title: Section.Body
linktitle: Body
articleTitle: Body
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Section Body qui récupère le nœud enfant Body, améliorant ainsi votre développement Web avec une gestion de contenu simplifiée.
type: docs
weight: 20
url: /fr/net/aspose.words/section/body/
---
## Section.Body property

Renvoie le[`Body`](../../body/) nœud enfant de la section.

```csharp
public Body Body { get; }
```

## Remarques

[`Body`](../../body/) contient le texte principal de la section.

Retours`nul` si la section n'a pas de[`Body`](../../body/) nœud parmi ses enfants.

## Exemples

Efface le texte principal de toutes les sections du document en laissant les sections elles-mêmes.

```csharp
Document doc = new Document();

// Un document vierge contient une section, un corps et un paragraphe.
// Appelez la méthode « RemoveAllChildren » pour supprimer tous ces nœuds,
// et se retrouver avec un nœud de document sans enfants.
doc.RemoveAllChildren();

// Ce document n'a désormais aucun nœud enfant composite auquel nous pouvons ajouter du contenu.
// Si nous souhaitons le modifier, nous devrons repeupler sa collection de nœuds.
// Tout d’abord, créez une nouvelle section, puis ajoutez-la en tant qu’enfant au nœud racine du document.
Section section = new Section(doc);
doc.AppendChild(section);

// Une section a besoin d'un corps, qui contiendra et affichera tout son contenu
// sur la page entre l'en-tête et le pied de page de la section.
Body body = new Body(doc);
section.AppendChild(body);

// Ce corps n'a pas d'enfants, nous ne pouvons donc pas encore y ajouter d'exécutions.
Assert.AreEqual(0, doc.FirstSection.Body.GetChildNodes(NodeType.Any, true).Count);

 // Appelez « EnsureMinimum » pour vous assurer que ce corps contient au moins un paragraphe vide.
body.EnsureMinimum();

// Maintenant, nous pouvons ajouter des exécutions au corps et faire en sorte que le document les affiche.
body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Voir également

* class [Body](../../body/)
* class [Section](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
