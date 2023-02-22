---
title: Node.GetText
second_title: Référence de l'API Aspose.Words pour .NET
description: Node méthode. Obtient le texte de ce nœud et de tous ses enfants.
type: docs
weight: 120
url: /fr/net/aspose.words/node/gettext/
---
## Node.GetText method

Obtient le texte de ce nœud et de tous ses enfants.

```csharp
public virtual string GetText()
```

### Remarques

La chaîne renvoyée comprend tous les caractères de contrôle et spéciaux, comme décrit dans[`ControlChar`](../../controlchar/).

### Exemples

Montre comment utiliser les caractères de contrôle.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer des paragraphes avec du texte avec DocumentBuilder.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// La conversion du document sous forme de texte révèle que les caractères de contrôle
// représentent certains des éléments structurels du document, tels que les sauts de page.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// Lors de la conversion d'un document sous forme de chaîne,
// nous pouvons omettre certains des caractères de contrôle avec la méthode Trim.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

Montre comment construire un document Aspose.Words à la main.

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

// Définit certaines propriétés de mise en page pour la section.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Une section a besoin d'un corps, qui contiendra et affichera tout son contenu
// sur la page entre l'en-tête et le pied de page de la section.
Body body = new Body(doc);
section.AppendChild(body);

// Crée un paragraphe, définit certaines propriétés de formatage, puis l'ajoute en tant qu'enfant au corps.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Enfin, ajoutez du contenu pour faire le document. Créer une course,
// définit son apparence et son contenu, puis l'ajoute en tant qu'enfant au paragraphe.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Voir également

* class [Node](../)
* espace de noms [Aspose.Words](../../node/)
* Assemblée [Aspose.Words](../../../)


