---
title: Section.Body
second_title: Référence de l'API Aspose.Words pour .NET
description: Section propriété. Renvoie le Corps nœud enfant de la section.
type: docs
weight: 20
url: /fr/net/aspose.words/section/body/
---
## Section.Body property

Renvoie le **Corps** nœud enfant de la section.

```csharp
public Body Body { get; }
```

### Remarques

**Corps** contient le texte principal de la section.

Renvoie null si la section n'a pas de **Corps** nœud parmi ses enfants.

### Exemples

Efface le texte principal de toutes les sections du document en laissant les sections elles-mêmes.

```csharp
Document doc = new Document();

// Un document vierge contient une section, un corps et un paragraphe.
// Appelez la méthode "RemoveAllChildren" pour supprimer tous ces nœuds,
// et se retrouver avec un nœud de document sans enfants.
doc.RemoveAllChildren();

// Ce document n'a plus de nœuds enfants composites auxquels nous pouvons ajouter du contenu.
// Si nous souhaitons l'éditer, nous devrons repeupler sa collection de nœuds.
// Tout d'abord, créez une nouvelle section, puis ajoutez-la en tant qu'enfant au nœud de document racine.
Section section = new Section(doc);
doc.AppendChild(section);

// Une section a besoin d'un corps, qui contiendra et affichera tout son contenu
// sur la page entre l'en-tête et le pied de page de la section.
Body body = new Body(doc);
section.AppendChild(body);

// Ce corps n'a pas d'enfants, nous ne pouvons donc pas encore lui ajouter d'exécutions.
Assert.AreEqual(0, doc.FirstSection.Body.GetChildNodes(NodeType.Any, true).Count);

// Appelez le "EnsureMinimum" pour vous assurer que ce corps contient au moins un paragraphe vide. 
body.EnsureMinimum();

// Maintenant, nous pouvons ajouter des passages au corps et faire en sorte que le document les affiche.
body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Voir également

* class [Body](../../body/)
* class [Section](../)
* espace de noms [Aspose.Words](../../section/)
* Assemblée [Aspose.Words](../../../)


