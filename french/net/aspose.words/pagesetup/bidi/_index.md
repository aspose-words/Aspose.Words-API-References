---
title: PageSetup.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words pour .NET
description: Découvrez la propriété PageSetup Bidi pour une mise en forme bidirectionnelle fluide du texte. Améliorez la lisibilité de vos documents grâce à la prise en charge de scripts complexes !
type: docs
weight: 10
url: /fr/net/aspose.words/pagesetup/bidi/
---
## PageSetup.Bidi property

Spécifie que cette section contient du texte bidirectionnel (scripts complexes).

```csharp
public bool Bidi { get; set; }
```

## Remarques

Quand`vrai`, les colonnes de cette section sont disposées de droite à gauche.

## Exemples

Montre comment définir l'ordre des colonnes de texte dans une section.

```csharp
Document doc = new Document();

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TextColumns.SetCount(3);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Write("Column 2.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Write("Column 3.");

// Définissez la propriété « Bidi » sur « true » pour organiser les colonnes en commençant par le côté droit de la page.
// L'ordre des colonnes correspondra à la direction du texte de droite à gauche.
// Définissez la propriété « Bidi » sur « false » pour organiser les colonnes en commençant par le côté gauche de la page.
// L'ordre des colonnes correspondra à la direction du texte de gauche à droite.
pageSetup.Bidi = reverseColumns;

doc.Save(ArtifactsDir + "PageSetup.Bidi.docx");
```

### Voir également

* class [PageSetup](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
