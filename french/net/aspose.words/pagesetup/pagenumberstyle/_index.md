---
title: PageSetup.PageNumberStyle
second_title: Référence de l'API Aspose.Words pour .NET
description: PageSetup propriété. Obtient ou définit le format du numéro de page.
type: docs
weight: 310
url: /fr/net/aspose.words/pagesetup/pagenumberstyle/
---
## PageSetup.PageNumberStyle property

Obtient ou définit le format du numéro de page.

```csharp
public NumberStyle PageNumberStyle { get; set; }
```

### Exemples

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

// Déplace le générateur de document vers l'en-tête principal de la première section,
// que chaque page de cette section affichera.
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// Insère un champ PAGE, qui affichera le numéro de la page en cours.
builder.Write("Page ");
builder.InsertField("PAGE", "");

// Configurez la section pour que le nombre de pages que les champs PAGE affichent commencent à 5.
// Configurez également tous les champs PAGE pour afficher leurs numéros de page en chiffres romains majuscules.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// Crée un autre en-tête principal pour la deuxième section, avec un autre champ PAGE.
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// Configurez la section pour que le nombre de pages que les champs PAGE affichent commence à 10.
// Configurez également tous les champs PAGE pour afficher leurs numéros de page en chiffres arabes.
pageSetup = doc.Sections[1].PageSetup;
pageSetup.PageStartingNumber = 10;
pageSetup.RestartPageNumbering = true;
pageSetup.PageNumberStyle = NumberStyle.Arabic;

doc.Save(ArtifactsDir + "PageSetup.PageNumbering.docx");
```

### Voir également

* enum [NumberStyle](../../numberstyle/)
* class [PageSetup](../)
* espace de noms [Aspose.Words](../../pagesetup/)
* Assemblée [Aspose.Words](../../../)


