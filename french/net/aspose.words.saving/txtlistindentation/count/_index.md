---
title: TxtListIndentation.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words pour .NET
description: TxtListIndentation Count propriété. Obtient ou définit combienCharacter à utiliser comme indentation pour un niveau de liste. La valeur par défaut est 0 cela signifie pas dindentation en C#.
type: docs
weight: 30
url: /fr/net/aspose.words.saving/txtlistindentation/count/
---
## TxtListIndentation.Count property

Obtient ou définit combien[`Character`](../character/) à utiliser comme indentation pour un niveau de liste. La valeur par défaut est 0, cela signifie pas d'indentation.

```csharp
public int Count { get; set; }
```

## Exemples

Montre comment configurer l’indentation de liste lors de l’enregistrement d’un document en texte brut.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crée une liste avec trois niveaux d'indentation.
builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Item 1");
builder.ListFormat.ListIndent();
builder.Writeln("Item 2");
builder.ListFormat.ListIndent(); 
builder.Write("Item 3");

// Crée un objet "TxtSaveOptions", que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont nous enregistrons le document en texte brut.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Définissez la propriété "Character" pour attribuer un caractère à utiliser
// pour un remplissage qui simule l'indentation de liste en texte brut.
txtSaveOptions.ListIndentation.Character = ' ';

// Définit la propriété "Count" pour spécifier le nombre de fois
// pour placer le caractère de remplissage pour chaque niveau de retrait de liste.
txtSaveOptions.ListIndentation.Count = 3;

doc.Save(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt");

Assert.AreEqual("1. Item 1\r\n" +
                "   a. Item 2\r\n" +
                "      i. Item 3\r\n", docText);
```

### Voir également

* class [TxtListIndentation](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
