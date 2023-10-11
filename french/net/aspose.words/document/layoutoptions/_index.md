---
title: Document.LayoutOptions
second_title: Référence de l'API Aspose.Words pour .NET
description: Document propriété. Obtient unLayoutOptions objet qui représente les options permettant de contrôler le processus de mise en page de ce document.
type: docs
weight: 250
url: /fr/net/aspose.words/document/layoutoptions/
---
## Document.LayoutOptions property

Obtient un[`LayoutOptions`](../../../aspose.words.layout/layoutoptions/) objet qui représente les options permettant de contrôler le processus de mise en page de ce document.

```csharp
public LayoutOptions LayoutOptions { get; }
```

### Exemples

Montre comment masquer le texte dans un document de sortie rendu.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Insère du texte masqué, puis précise si nous souhaitons l'omettre d'un document rendu.
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
// Ajoutez quelques paragraphes, puis activez les marques de paragraphe pour afficher la fin des paragraphes
// avec un symbole pillcrow (¶) lorsque nous rendons le document.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

Montre comment modifier l’apparence des révisions dans un document de sortie rendu.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère une révision, puis change la couleur de toutes les révisions en vert.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Supprime la barre qui apparaît à gauche de chaque ligne révisée.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### Voir également

* class [LayoutOptions](../../../aspose.words.layout/layoutoptions/)
* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)


