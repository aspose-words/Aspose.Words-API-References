---
title: SaveOptions.UpdateAmbiguousTextFont
linktitle: UpdateAmbiguousTextFont
articleTitle: UpdateAmbiguousTextFont
second_title: Aspose.Words pour .NET
description: Améliorez la clarté du texte dans vos PDF avec UpdateAmbiguousTextFont. Assurez un rendu précis des polices basé sur les codes de caractères pour une meilleure lisibilité.
type: docs
weight: 150
url: /fr/net/aspose.words.saving/saveoptions/updateambiguoustextfont/
---
## SaveOptions.UpdateAmbiguousTextFont property

Détermine si les attributs de police seront modifiés en fonction du code de caractère utilisé.

```csharp
public bool UpdateAmbiguousTextFont { get; set; }
```

## Exemples

Montre comment mettre à jour la police pour qu'elle corresponde au code de caractère utilisé.

```csharp
Document doc = new Document(MyDir + "Special symbol.docx");
Run run = doc.FirstSection.Body.FirstParagraph.Runs[0];
Console.WriteLine(run.Text); // ฿
Console.WriteLine(run.Font.Name); // Arial

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.UpdateAmbiguousTextFont = true;
doc.Save(ArtifactsDir + "OoxmlSaveOptions.UpdateAmbiguousTextFont.docx", saveOptions);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.UpdateAmbiguousTextFont.docx");
run = doc.FirstSection.Body.FirstParagraph.Runs[0];
Console.WriteLine(run.Text); // ฿
Console.WriteLine(run.Font.Name); // Angsana Nouveau
```

### Voir également

* class [SaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
