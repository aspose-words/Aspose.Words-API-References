---
title: Node.GetText
linktitle: GetText
articleTitle: GetText
second_title: Aspose.Words pour .NET
description: Découvrez la méthode Node GetText pour récupérer sans effort du texte à partir d'un nœud et de ses éléments enfants, améliorant ainsi votre gestion des données et l'efficacité de votre développement.
type: docs
weight: 120
url: /fr/net/aspose.words/node/gettext/
---
## Node.GetText method

Obtient le texte de ce nœud et de tous ses enfants.

```csharp
public virtual string GetText()
```

## Remarques

La chaîne renvoyée inclut tous les caractères de contrôle et spéciaux comme décrit dans[`ControlChar`](../../controlchar/).

## Exemples

Montre comment utiliser les caractères de contrôle.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer des paragraphes avec du texte avec DocumentBuilder.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// La conversion du document au format texte révèle que les caractères de contrôle
// représentent certains des éléments structurels du document, tels que les sauts de page.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// Lors de la conversion d'un document au format chaîne,
// nous pouvons omettre certains des caractères de contrôle avec la méthode Trim.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

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

* class [Node](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
