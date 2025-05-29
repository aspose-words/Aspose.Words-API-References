---
title: PdfSaveOptions.CreateNoteHyperlinks
linktitle: CreateNoteHyperlinks
articleTitle: CreateNoteHyperlinks
second_title: Aspose.Words pour .NET
description: Améliorez vos PDF avec les hyperliens CreateNote de PdfSaveOptions. Convertissez les notes de bas de page et de fin en liens cliquables pour une navigation simplifiée. Valeur par défaut : false.
type: docs
weight: 60
url: /fr/net/aspose.words.saving/pdfsaveoptions/createnotehyperlinks/
---
## PdfSaveOptions.CreateNoteHyperlinks property

Spécifie s'il faut convertir les références de notes de bas de page/de fin de texte dans l'article principal en hyperliens actifs. Lorsqu'il est cliqué, l'hyperlien mènera à la note de bas de page/de fin correspondante. La valeur par défaut est`FAUX` .

```csharp
public bool CreateNoteHyperlinks { get; set; }
```

## Exemples

Montre comment faire fonctionner les notes de bas de page et les notes de fin comme des hyperliens.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Définissez la propriété « CreateNoteHyperlinks » sur « true » pour activer tous les symboles de note de bas de page/de fin
// dans le texte agissent comme des liens qui, en cliquant, nous amènent à leurs notes de bas de page/notes de fin respectives.
// Définissez la propriété « CreateNoteHyperlinks » sur « false » pour que les symboles de note de bas de page/de fin ne soient pas liés à quoi que ce soit.
options.CreateNoteHyperlinks = createNoteHyperlinks;

doc.Save(ArtifactsDir + "PdfSaveOptions.NoteHyperlinks.pdf", options);
```

### Voir également

* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
