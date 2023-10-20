---
title: PageSetup.BorderSurroundsFooter
linktitle: BorderSurroundsFooter
articleTitle: BorderSurroundsFooter
second_title: Aspose.Words pour .NET
description: PageSetup BorderSurroundsFooter propriété. Spécifie si la bordure de la page inclut ou exclut le pied de page en C#.
type: docs
weight: 60
url: /fr/net/aspose.words/pagesetup/bordersurroundsfooter/
---
## PageSetup.BorderSurroundsFooter property

Spécifie si la bordure de la page inclut ou exclut le pied de page.

```csharp
public bool BorderSurroundsFooter { get; set; }
```

## Remarques

Notez que la modification de cette propriété affecte toutes les sections du document.

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

// Insère une bordure bleue à double ligne.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.Borders.LineStyle = LineStyle.Double;
pageSetup.Borders.Color = Color.Blue;

// L'objet PageSetup d'une section possède les indicateurs "BorderSurroundsHeader" et "BorderSurroundsFooter" qui déterminent
// si une bordure de page entoure le corps du texte principal, inclut également respectivement l'en-tête ou le pied de page.
// Met le flag "BorderSurroundsHeader" à "true" pour entourer l'en-tête de notre bordure,
// puis définissez l'indicateur "BorderSurroundsFooter" pour laisser le pied de page en dehors de la bordure.
pageSetup.BorderSurroundsHeader = true;
pageSetup.BorderSurroundsFooter = false;

doc.Save(ArtifactsDir + "PageSetup.PageBorder.docx");
```

### Voir également

* class [PageSetup](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
