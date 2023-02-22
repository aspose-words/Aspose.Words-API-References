---
title: PageSetup.PageStartingNumber
second_title: Référence de l'API Aspose.Words pour .NET
description: PageSetup propriété. Obtient ou définit le numéro de page de début de la section.
type: docs
weight: 320
url: /fr/net/aspose.words/pagesetup/pagestartingnumber/
---
## PageSetup.PageStartingNumber property

Obtient ou définit le numéro de page de début de la section.

```csharp
public int PageStartingNumber { get; set; }
```

### Remarques

Le[`RestartPageNumbering`](../restartpagenumbering/) propriété, si elle est définie sur **faux** , remplacera the  **PageStartingNumber** propriété afin que la numérotation des pages puisse continuer à partir de la section précédente.

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

* class [PageSetup](../)
* espace de noms [Aspose.Words](../../pagesetup/)
* Assemblée [Aspose.Words](../../../)


