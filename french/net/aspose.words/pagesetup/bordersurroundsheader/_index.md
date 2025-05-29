---
title: PageSetup.BorderSurroundsHeader
linktitle: BorderSurroundsHeader
articleTitle: BorderSurroundsHeader
second_title: Aspose.Words pour .NET
description: Découvrez la propriété PageSetup BorderSurroundsHeader pour personnaliser les bordures de vos pages. Contrôlez l'inclusion des en-têtes pour une mise en page soignée.
type: docs
weight: 70
url: /fr/net/aspose.words/pagesetup/bordersurroundsheader/
---
## PageSetup.BorderSurroundsHeader property

Spécifie si la bordure de la page inclut ou exclut l'en-tête.

```csharp
public bool BorderSurroundsHeader { get; set; }
```

## Remarques

Remarque : la modification de cette propriété affecte toutes les sections du document.

## Exemples

Montre comment appliquer une bordure à la page et à l'en-tête/pied de page.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This is the main body text.");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer.");
builder.MoveToDocumentEnd();

// Insérer une bordure à double ligne bleue.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.Borders.LineStyle = LineStyle.Double;
pageSetup.Borders.Color = Color.Blue;

// L'objet PageSetup d'une section possède les indicateurs « BorderSurroundsHeader » et « BorderSurroundsFooter » qui déterminent
// si une bordure de page entoure le texte du corps principal, inclut également l'en-tête ou le pied de page, respectivement.
// Définissez l'indicateur « BorderSurroundsHeader » sur « true » pour entourer l'en-tête avec notre bordure,
// puis définissez l'indicateur « BorderSurroundsFooter » pour laisser le pied de page en dehors de la bordure.
pageSetup.BorderSurroundsHeader = true;
pageSetup.BorderSurroundsFooter = false;

doc.Save(ArtifactsDir + "PageSetup.PageBorder.docx");
```

### Voir également

* class [PageSetup](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
