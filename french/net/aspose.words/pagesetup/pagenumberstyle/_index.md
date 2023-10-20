---
title: PageSetup.PageNumberStyle
linktitle: PageNumberStyle
articleTitle: PageNumberStyle
second_title: Aspose.Words pour .NET
description: PageSetup PageNumberStyle propriété. Obtient ou définit le format du numéro de page en C#.
type: docs
weight: 320
url: /fr/net/aspose.words/pagesetup/pagenumberstyle/
---
## PageSetup.PageNumberStyle property

Obtient ou définit le format du numéro de page.

```csharp
public NumberStyle PageNumberStyle { get; set; }
```

## Exemples

Montre comment configurer la numérotation des pages dans une section.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 3.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("Section 2, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 3.");

// Déplace le générateur de documents vers l'en-tête principal de la première section,
// que chaque page de cette section affichera.
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// Insère un champ PAGE, qui affichera le numéro de la page en cours.
builder.Write("Page ");
builder.InsertField("PAGE", "");

// Configurez la section pour que le nombre de pages affiché par les champs PAGE commence à 5.
// Configurez également tous les champs PAGE pour afficher leurs numéros de page en utilisant des chiffres romains majuscules.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// Créez un autre en-tête principal pour la deuxième section, avec un autre champ PAGE.
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// Configurez la section pour que le nombre de pages affiché par les champs PAGE commence à 10.
// Configurez également tous les champs PAGE pour afficher leurs numéros de page en utilisant des chiffres arabes.
pageSetup = doc.Sections[1].PageSetup;
pageSetup.PageStartingNumber = 10;
pageSetup.RestartPageNumbering = true;
pageSetup.PageNumberStyle = NumberStyle.Arabic;

doc.Save(ArtifactsDir + "PageSetup.PageNumbering.docx");
```

### Voir également

* enum [NumberStyle](../../numberstyle/)
* class [PageSetup](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
