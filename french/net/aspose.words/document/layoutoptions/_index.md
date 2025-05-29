---
title: Document.LayoutOptions
linktitle: LayoutOptions
articleTitle: LayoutOptions
second_title: Aspose.Words pour .NET
description: Explorez la propriété « Document LayoutOptions » pour contrôler efficacement la mise en page de votre document. Profitez d'options de conception flexibles pour une présentation optimale.
type: docs
weight: 260
url: /fr/net/aspose.words/document/layoutoptions/
---
## Document.LayoutOptions property

Obtient un[`LayoutOptions`](../../../aspose.words.layout/layoutoptions/) objet qui représente les options permettant de contrôler le processus de mise en page de ce document.

```csharp
public LayoutOptions LayoutOptions { get; }
```

## Exemples

Montre comment masquer du texte dans un document de sortie rendu.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Insérer du texte masqué, puis spécifier si nous souhaitons l'omettre d'un document rendu.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

Montre comment afficher les marques de paragraphe dans un document de sortie rendu.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Ajoutez quelques paragraphes, puis activez les marques de paragraphe pour afficher les fins de paragraphes
// avec un symbole pilcrow (¶) lorsque nous rendons le document.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

Montre comment modifier l’apparence des révisions dans un document de sortie rendu.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérez une révision, puis changez la couleur de toutes les révisions en vert.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Supprimez la barre qui apparaît à gauche de chaque ligne révisée.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;
doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;

doc.Save(ArtifactsDir + "Revision.LayoutOptionsRevisions.pdf");
```

### Voir également

* class [LayoutOptions](../../../aspose.words.layout/layoutoptions/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
