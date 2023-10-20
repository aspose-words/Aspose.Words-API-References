---
title: CleanupOptions.DuplicateStyle
linktitle: DuplicateStyle
articleTitle: DuplicateStyle
second_title: Aspose.Words pour .NET
description: CleanupOptions DuplicateStyle propriété. Obtient/définit un indicateur indiquant si les styles en double doivent être supprimés du document. La valeur par défaut estFAUX  en C#.
type: docs
weight: 20
url: /fr/net/aspose.words/cleanupoptions/duplicatestyle/
---
## CleanupOptions.DuplicateStyle property

Obtient/définit un indicateur indiquant si les styles en double doivent être supprimés du document. La valeur par défaut est`FAUX` .

```csharp
public bool DuplicateStyle { get; set; }
```

## Exemples

Montre comment supprimer les styles dupliqués du document.

```csharp
Document doc = new Document();

// Ajout de deux styles au document avec des propriétés identiques,
// mais des noms différents. Le deuxième style est considéré comme un double du premier.
Style myStyle = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

Style duplicateStyle = doc.Styles.Add(StyleType.Paragraph, "MyStyle2");
duplicateStyle.Font.Size = 14;
duplicateStyle.Font.Name = "Courier New";
duplicateStyle.Font.Color = Color.Blue;

Assert.AreEqual(6, doc.Styles.Count);

// Applique les deux styles à différents paragraphes du document.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

builder.ParagraphFormat.StyleName = duplicateStyle.Name;
builder.Writeln("Hello again!");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(myStyle, paragraphs[0].ParagraphFormat.Style);
Assert.AreEqual(duplicateStyle, paragraphs[1].ParagraphFormat.Style);

// Configurez un objet CleanOptions, puis appelez la méthode Cleanup pour remplacer tous les styles en double
// avec l'original et supprime les doublons du document.
CleanupOptions cleanupOptions = new CleanupOptions { DuplicateStyle = true };

doc.Cleanup(cleanupOptions);

Assert.AreEqual(5, doc.Styles.Count);
Assert.AreEqual(myStyle, paragraphs[0].ParagraphFormat.Style);
Assert.AreEqual(myStyle, paragraphs[1].ParagraphFormat.Style);
```

### Voir également

* class [CleanupOptions](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
