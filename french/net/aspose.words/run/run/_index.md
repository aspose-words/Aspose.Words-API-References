---
title: Run
linktitle: Run
articleTitle: Run
second_title: Aspose.Words pour .NET
description: Créez et personnalisez facilement votre instance de classe Run. Bénéficiez de fonctionnalités puissantes pour des performances optimisées et des fonctionnalités améliorées.
type: docs
weight: 10
url: /fr/net/aspose.words/run/run/
---
## Run(*[DocumentBase](../../documentbase/)*) {#constructor}

Initialise une nouvelle instance du[`Run`](../) classe.

```csharp
public Run(DocumentBase doc)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| doc | DocumentBase | Le document du propriétaire. |

## Remarques

Quand[`Run`](../) est créé, il appartient au document spécifié, mais ne fait pas encore partie du document et[`ParentNode`](../../node/parentnode/) est`nul`.

Pour ajouter[`Run`](../) à l'utilisation du document[`InsertAfter`](../../compositenode/insertafter/) ou[`InsertBefore`](../../compositenode/insertbefore/) sur le paragraphe où vous souhaitez insérer l'exécution.

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

* class [DocumentBase](../../documentbase/)
* class [Run](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## Run(*[DocumentBase](../../documentbase/), string*) {#constructor_1}

Initialise une nouvelle instance du**Courir** classe.

```csharp
public Run(DocumentBase doc, string text)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| doc | DocumentBase | Le document du propriétaire. |
| text | String | Le texte de la course. |

## Remarques

Quand[`Run`](../) est créé, il appartient au document spécifié, mais ne fait pas encore partie du document et[`ParentNode`](../../node/parentnode/) est`nul`.

Pour ajouter[`Run`](../) à l'utilisation du document[`InsertAfter`](../../compositenode/insertafter/) ou[`InsertBefore`](../../compositenode/insertbefore/) sur le paragraphe où vous souhaitez insérer l'exécution.

## Exemples

Montre comment formater une série de texte à l'aide de sa propriété de police.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

### Voir également

* class [DocumentBase](../../documentbase/)
* class [Run](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
