---
title: TxtSaveOptions.AddBidiMarks
second_title: Référence de l'API Aspose.Words pour .NET
description: TxtSaveOptions propriété. Spécifie sil faut ajouter des marques bidirectionnelles avant chaque exécution de BiDi lors de lexportation au format texte brut.
type: docs
weight: 20
url: /fr/net/aspose.words.saving/txtsaveoptions/addbidimarks/
---
## TxtSaveOptions.AddBidiMarks property

Spécifie s'il faut ajouter des marques bidirectionnelles avant chaque exécution de BiDi lors de l'exportation au format texte brut.

La valeur par défaut est`FAUX`.

```csharp
public bool AddBidiMarks { get; set; }
```

### Exemples

Montre comment insérer le caractère Unicode « MARQUE DE DROITE À GAUCHE » (U+200F) avant chaque exécution bidirectionnelle dans le texte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.ParagraphFormat.Bidi = true;
builder.Writeln("שלום עולם!");
builder.Writeln("مرحبا بالعالم!");

// Crée un objet "TxtSaveOptions", que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont nous enregistrons le document en texte brut.
TxtSaveOptions saveOptions = new TxtSaveOptions { Encoding = System.Text.Encoding.Unicode};

// Définissez la propriété "AddBidiMarks" sur "true" pour ajouter des marques avant les exécutions
// avec un texte de droite à gauche pour indiquer le fait.
// Définissez la propriété "AddBidiMarks" sur "false" pour écrire tout de gauche à droite
// et de droite à gauche s'exécutent de la même manière sans rien pour indiquer lequel est lequel.
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
* espace de noms [Aspose.Words.Saving](../../txtsaveoptions/)
* Assemblée [Aspose.Words](../../../)


