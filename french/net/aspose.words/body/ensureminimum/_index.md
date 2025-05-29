---
title: Body.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words pour .NET
description: Optimisez votre contenu avec la méthode Body EnsureMinimum. Ajoutez automatiquement un paragraphe vide si le dernier enfant n'est pas un paragraphe pour une meilleure mise en forme.
type: docs
weight: 70
url: /fr/net/aspose.words/body/ensureminimum/
---
## Body.EnsureMinimum method

Si le dernier enfant n'est pas un paragraphe, crée et ajoute un paragraphe vide.

```csharp
public void EnsureMinimum()
```

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

* class [Body](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
