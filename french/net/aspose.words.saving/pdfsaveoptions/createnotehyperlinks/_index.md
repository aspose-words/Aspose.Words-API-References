---
title: PdfSaveOptions.CreateNoteHyperlinks
linktitle: CreateNoteHyperlinks
articleTitle: CreateNoteHyperlinks
second_title: Aspose.Words pour .NET
description: PdfSaveOptions CreateNoteHyperlinks propriété. Spécifie sil faut convertir les références de note de bas de page/note de fin dans lhistoire du texte principal en hyperliens actifs. Lorsque vous cliquez dessus le lien hypertexte mènera à la note de bas de page/note de fin correspondante. La valeur par défaut estFAUX  en C#.
type: docs
weight: 50
url: /fr/net/aspose.words.saving/pdfsaveoptions/createnotehyperlinks/
---
## PdfSaveOptions.CreateNoteHyperlinks property

Spécifie s'il faut convertir les références de note de bas de page/note de fin dans l'histoire du texte principal en hyperliens actifs. Lorsque vous cliquez dessus, le lien hypertexte mènera à la note de bas de page/note de fin correspondante. La valeur par défaut est`FAUX` .

```csharp
public bool CreateNoteHyperlinks { get; set; }
```

## Exemples

Montre comment faire en sorte que les notes de bas de page et les notes de fin fonctionnent comme des hyperliens.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

// Crée un objet "PdfSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Définissez la propriété "CreateNoteHyperlinks" sur "true" pour activer tous les symboles de note de bas de page/note de fin
// dans le texte agissent comme des liens qui, en cliquant, nous amènent à leurs notes de bas de page/notes de fin respectives.
// Définissez la propriété "CreateNoteHyperlinks" sur "false" pour que les symboles de note de bas de page/note de fin ne soient pas liés à quoi que ce soit.
options.CreateNoteHyperlinks = createNoteHyperlinks;

doc.Save(ArtifactsDir + "PdfSaveOptions.NoteHyperlinks.pdf", options);
```

### Voir également

* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
