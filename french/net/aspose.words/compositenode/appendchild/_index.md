---
title: CompositeNode.AppendChild
linktitle: AppendChild
articleTitle: AppendChild
second_title: Aspose.Words pour .NET
description: CompositeNode AppendChild méthode. Ajoute le nœud spécifié à la fin de la liste des nœuds enfants pour ce nœud en C#.
type: docs
weight: 60
url: /fr/net/aspose.words/compositenode/appendchild/
---
## CompositeNode.AppendChild method

Ajoute le nœud spécifié à la fin de la liste des nœuds enfants pour ce nœud.

```csharp
public Node AppendChild(Node newChild)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| newChild | Node | Le nœud à ajouter. |

### Return_Value

Le nœud ajouté.

## Remarques

Si la*newChild* est déjà dans l'arborescence, il est d'abord supprimé.

Si le nœud en cours d'insertion a été créé à partir d'un autre document, vous devez utiliser [`ImportNode`](../../documentbase/importnode/) pour importer le nœud dans le document actuel. Le nœud importé peut ensuite être inséré dans le document actuel.

## Exemples

Montre comment construire manuellement un document Aspose.Words.

```csharp
Document doc = new Document();

// Un document vierge contient une section, un corps et un paragraphe.
// Appelez la méthode "RemoveAllChildren" pour supprimer tous ces nœuds,
// et on se retrouve avec un nœud de document sans enfants.
doc.RemoveAllChildren();

// Ce document n'a désormais aucun nœud enfant composite auquel nous pouvons ajouter du contenu.
// Si nous souhaitons le modifier, nous devrons repeupler sa collection de nœuds.
// Commencez par créer une nouvelle section, puis ajoutez-la en tant qu'enfant au nœud du document racine.
Section section = new Section(doc);
doc.AppendChild(section);

// Définissez certaines propriétés de mise en page pour la section.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Une section a besoin d'un corps, qui contiendra et affichera tout son contenu
// sur la page entre l'en-tête et le pied de page de la section.
Body body = new Body(doc);
section.AppendChild(body);

// Créez un paragraphe, définissez certaines propriétés de mise en forme, puis ajoutez-le en tant qu'enfant au corps.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Enfin, ajoutez du contenu pour faire le document. Créez une course,
// définit son apparence et son contenu, puis l'ajoute en tant qu'enfant au paragraphe.
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
