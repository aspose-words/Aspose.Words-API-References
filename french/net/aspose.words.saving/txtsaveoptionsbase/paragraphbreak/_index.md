---
title: TxtSaveOptionsBase.ParagraphBreak
linktitle: ParagraphBreak
articleTitle: ParagraphBreak
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ParagraphBreak de TxtSaveOptionsBase, qui permet des sauts de paragraphe personnalisés pour des exportations fluides au format texte. Améliorez la lisibilité de votre document !
type: docs
weight: 40
url: /fr/net/aspose.words.saving/txtsaveoptionsbase/paragraphbreak/
---
## TxtSaveOptionsBase.ParagraphBreak property

Spécifie la chaîne à utiliser comme saut de paragraphe lors de l'exportation au format texte.

```csharp
public string ParagraphBreak { get; set; }
```

## Remarques

La valeur par défaut est[`CrLf`](../../../aspose.words/controlchar/crlf/).

## Exemples

Montre comment enregistrer un document .txt avec un saut de paragraphe personnalisé.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");
builder.Write("Paragraph 3.");

// Créez un objet « TxtSaveOptions », que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la façon dont nous enregistrons le document en texte brut.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

Assert.AreEqual(SaveFormat.Text, txtSaveOptions.SaveFormat);

// Définissez le « ParagraphBreak » sur une valeur personnalisée que nous souhaitons placer à la fin de chaque paragraphe.
txtSaveOptions.ParagraphBreak = " End of paragraph.\n\n\t";

doc.Save(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt");

Assert.AreEqual("Paragraph 1. End of paragraph.\n\n\t" +
                "Paragraph 2. End of paragraph.\n\n\t" +
                "Paragraph 3. End of paragraph.\n\n\t", docText);
```

### Voir également

* class [TxtSaveOptionsBase](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
