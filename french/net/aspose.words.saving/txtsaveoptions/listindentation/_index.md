---
title: TxtSaveOptions.ListIndentation
linktitle: ListIndentation
articleTitle: ListIndentation
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ListIndentation de TxtSaveOptions, qui personnalise l'indentation des listes pour une meilleure lisibilité. Contrôlez les caractères et les niveaux sans effort !
type: docs
weight: 30
url: /fr/net/aspose.words.saving/txtsaveoptions/listindentation/
---
## TxtSaveOptions.ListIndentation property

Obtient un[`TxtListIndentation`](../../txtlistindentation/)objet qui spécifie combien et quel caractère utiliser pour l'indentation des niveaux de liste. Par défaut, le nombre de caractères '\0' est nul, ce qui signifie aucune indentation.

```csharp
public TxtListIndentation ListIndentation { get; }
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

* class [TxtListIndentation](../../txtlistindentation/)
* class [TxtSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
