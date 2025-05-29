---
title: CompositeNode.AppendChild
linktitle: AppendChild
articleTitle: AppendChild
second_title: Aspose.Words pour .NET
description: Découvrez comment la méthode CompositeNode AppendChild améliore votre codage en ajoutant facilement des nœuds à votre liste de nœuds enfants. Optimisez votre efficacité de développement !
type: docs
weight: 80
url: /fr/net/aspose.words/compositenode/appendchild/
---
## CompositeNode.AppendChild&lt;T&gt; method

Ajoute le nœud spécifié à la fin de la liste des nœuds enfants pour ce nœud.

```csharp
public T AppendChild<T>(T newChild)
    where T : Node
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| newChild | T | Le nœud à ajouter. |

### Return_Value

Le nœud a été ajouté.

## Remarques

Si le*newChild* est déjà dans l'arbre, il est d'abord supprimé.

Si le nœud inséré a été créé à partir d'un autre document, vous devez utiliser [`ImportNode`](../../documentbase/importnode/) pour importer le nœud dans le document actuel. Le nœud importé peut ensuite être inséré dans le document actuel.

## Exemples

Montre comment construire un document Aspose.Words à la main.

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

// Définissez certaines propriétés de configuration de page pour la section.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Une section a besoin d'un corps, qui contiendra et affichera tout son contenu
// sur la page entre l'en-tête et le pied de page de la section.
Body body = new Body(doc);
section.AppendChild(body);

// Créez un paragraphe, définissez certaines propriétés de formatage, puis ajoutez-le en tant qu'enfant au corps.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Enfin, ajoutez du contenu pour compléter le document. Créez une exécution,
// définissez son apparence et son contenu, puis ajoutez-le en tant qu'enfant au paragraphe.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Voir également

* class [Node](../../node/)
* class [CompositeNode](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
