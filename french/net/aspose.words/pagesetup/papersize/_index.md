---
title: PageSetup.PaperSize
linktitle: PaperSize
articleTitle: PaperSize
second_title: Aspose.Words pour .NET
description: Découvrez la propriété PageSetup PaperSize pour personnaliser et gérer facilement le format de papier de votre document pour des résultats d'impression optimaux.
type: docs
weight: 350
url: /fr/net/aspose.words/pagesetup/papersize/
---
## PageSetup.PaperSize property

Renvoie ou définit le format du papier.

```csharp
public PaperSize PaperSize { get; set; }
```

## Remarques

La définition de cette propriété met à jour[`PageWidth`](../pagewidth/) et[`PageHeight`](../pageheight/) valeurs. Définition de cette valeur surCustom ne modifie pas les valeurs existantes.

## Exemples

Montre comment définir le format de papier de JisB4 ou JisB5.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

PageSetup pageSetup = doc.FirstSection.PageSetup;
// Définissez la taille du papier sur JisB4 (257x364mm).
pageSetup.PaperSize = PaperSize.JisB4;
// Vous pouvez également définir le format du papier sur JisB5. (182x257mm).
pageSetup.PaperSize = PaperSize.JisB5;
```

Montre comment ajuster la taille du papier, l'orientation, les marges, ainsi que d'autres paramètres pour une section.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.PageSetup.PaperSize = PaperSize.Legal;
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.BottomMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.LeftMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.HeaderDistance = ConvertUtil.InchToPoint(0.2);
builder.PageSetup.FooterDistance = ConvertUtil.InchToPoint(0.2);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PageSetup.PageMargins.docx");
```

Montre comment définir les tailles de page.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nous pouvons modifier la taille de la page actuelle à une taille prédéfinie
// en utilisant la propriété « PaperSize » de l'objet PageSetup de cette section.
builder.PageSetup.PaperSize = PaperSize.Tabloid;

Assert.AreEqual(792.0d, builder.PageSetup.PageWidth);
Assert.AreEqual(1224.0d, builder.PageSetup.PageHeight);

builder.Writeln($"This page is {builder.PageSetup.PageWidth}x{builder.PageSetup.PageHeight}.");

// Chaque section possède son propre objet PageSetup. Lorsqu'on utilise un générateur de documents pour créer une nouvelle section,
// l'objet PageSetup de cette section hérite de toutes les valeurs de l'objet PageSetup de la section précédente.
builder.InsertBreak(BreakType.SectionBreakEvenPage);

Assert.AreEqual(PaperSize.Tabloid, builder.PageSetup.PaperSize);

builder.PageSetup.PaperSize = PaperSize.A5;
builder.Writeln($"This page is {builder.PageSetup.PageWidth}x{builder.PageSetup.PageHeight}.");

Assert.AreEqual(419.55d, builder.PageSetup.PageWidth);
Assert.AreEqual(595.30d, builder.PageSetup.PageHeight);

builder.InsertBreak(BreakType.SectionBreakEvenPage);

// Définissez une taille personnalisée pour les pages de cette section.
builder.PageSetup.PageWidth = 620;
builder.PageSetup.PageHeight = 480;

Assert.AreEqual(PaperSize.Custom, builder.PageSetup.PaperSize);

builder.Writeln($"This page is {builder.PageSetup.PageWidth}x{builder.PageSetup.PageHeight}.");

doc.Save(ArtifactsDir + "PageSetup.PaperSizes.docx");
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

* enum [PaperSize](../../papersize/)
* class [PageSetup](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
