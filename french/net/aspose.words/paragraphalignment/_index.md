---
title: ParagraphAlignment Enum
linktitle: ParagraphAlignment
articleTitle: ParagraphAlignment
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.ParagraphAlignment pour un alignement précis du texte dans vos documents. Améliorez la lisibilité et la mise en forme en toute simplicité !
type: docs
weight: 5130
url: /fr/net/aspose.words/paragraphalignment/
---
## ParagraphAlignment enumeration

Spécifie l'alignement du texte dans un paragraphe.

```csharp
public enum ParagraphAlignment
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Left | `0` | Le texte est aligné à gauche. |
| Center | `1` | Le texte est centré horizontalement. |
| Right | `2` | Le texte est aligné à droite. |
| Justify | `3` | Le texte est aligné à gauche et à droite. |
| Distributed | `4` | Le texte est réparti uniformément. |
| ArabicMediumKashida | `5` | Arabe uniquement. La longueur du texte en kashida est étendue à une longueur moyenne déterminée par l'utilisateur. |
| ArabicHighKashida | `7` | Arabe uniquement. La longueur du texte en kashida est étendue au maximum. |
| ArabicLowKashida | `8` | Arabe uniquement. La longueur du texte en kashida a été légèrement allongée. |
| ThaiDistributed | `9` | Thaï uniquement. Le texte est justifié avec une optimisation pour le thaï. |
| MathElementCenterAsGroup | `10` | Le seul élément mathématique d'une ligne, aligné comme « Centré en tant que groupe ». |

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

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
