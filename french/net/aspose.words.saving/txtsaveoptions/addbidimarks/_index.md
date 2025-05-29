---
title: TxtSaveOptions.AddBidiMarks
linktitle: AddBidiMarks
articleTitle: AddBidiMarks
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété TxtSaveOptions AddBidiMarks améliore les exportations de texte brut en ajoutant des marques bidirectionnelles pour une meilleure lisibilité et un meilleur formatage.
type: docs
weight: 20
url: /fr/net/aspose.words.saving/txtsaveoptions/addbidimarks/
---
## TxtSaveOptions.AddBidiMarks property

Spécifie s'il faut ajouter des marques bidirectionnelles avant chaque exécution BiDi lors de l'exportation au format texte brut.

La valeur par défaut est`FAUX`.

```csharp
public bool AddBidiMarks { get; set; }
```

## Exemples

Montre comment insérer le caractère Unicode « MARQUE DE DROITE À GAUCHE » (U+200F) avant chaque exécution bidirectionnelle dans le texte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.ParagraphFormat.Bidi = true;
builder.Writeln("שלום עולם!");
builder.Writeln("مرحبا بالعالم!");

// Créez un objet « TxtSaveOptions », que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la façon dont nous enregistrons le document en texte brut.
TxtSaveOptions saveOptions = new TxtSaveOptions { Encoding = System.Text.Encoding.Unicode};

// Définissez la propriété « AddBidiMarks » sur « true » pour ajouter des marques avant les exécutions
// avec du texte de droite à gauche pour indiquer le fait.
// Définissez la propriété « AddBidiMarks » sur « false » pour tout écrire de gauche à droite
// et de droite à gauche fonctionnent de manière égale sans rien pour indiquer lequel est lequel.
saveOptions.AddBidiMarks = addBidiMarks;

doc.Save(ArtifactsDir + "TxtSaveOptions.AddBidiMarks.txt", saveOptions);

string docText = System.Text.Encoding.Unicode.GetString(File.ReadAllBytes(ArtifactsDir + "TxtSaveOptions.AddBidiMarks.txt"));

if (addBidiMarks)
{
    Assert.AreEqual("\uFEFFHello world!‎\r\nשלום עולם!‏\r\nمرحبا بالعالم!‏\r\n\r\n", docText);
    Assert.True(docText.Contains("\u200f"));
}
else
{
    Assert.AreEqual("\uFEFFHello world!\r\nשלום עולם!\r\nمرحبا بالعالم!\r\n\r\n", docText);
    Assert.False(docText.Contains("\u200f"));
}
```

### Voir également

* class [TxtSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
