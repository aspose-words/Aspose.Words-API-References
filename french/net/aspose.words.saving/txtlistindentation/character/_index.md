---
title: TxtListIndentation.Character
linktitle: Character
articleTitle: Character
second_title: Aspose.Words pour .NET
description: Découvrez la propriété TxtListIndentation pour personnaliser l'indentation de vos listes avec votre caractère préféré. Améliorez la lisibilité et l'attrait visuel sans effort !
type: docs
weight: 20
url: /fr/net/aspose.words.saving/txtlistindentation/character/
---
## TxtListIndentation.Character property

Obtient ou définit le caractère à utiliser pour l'indentation des niveaux de liste. La valeur par défaut est '\0', ce qui signifie qu'il n'y a pas d'indentation.

```csharp
public char Character { get; set; }
```

## Exemples

Montre comment configurer le retrait de la liste lors de l'enregistrement d'un document en texte brut.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Créez une liste avec trois niveaux d'indentation.
builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Item 1");
builder.ListFormat.ListIndent();
builder.Writeln("Item 2");
builder.ListFormat.ListIndent(); 
builder.Write("Item 3");

// Créez un objet « TxtSaveOptions », que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la façon dont nous enregistrons le document en texte brut.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Définissez la propriété « Caractère » pour attribuer un caractère à utiliser
// pour le remplissage qui simule l'indentation de la liste en texte brut.
txtSaveOptions.ListIndentation.Character = ' ';

// Définissez la propriété « Count » pour spécifier le nombre de fois
// pour placer le caractère de remplissage pour chaque niveau de retrait de liste.
txtSaveOptions.ListIndentation.Count = 3;

doc.Save(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt");
string newLine= Environment.NewLine;

Assert.AreEqual($"1. Item 1{newLine}" +
                $"   a. Item 2{newLine}" +
                $"      i. Item 3{newLine}", docText);
```

### Voir également

* class [TxtListIndentation](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
