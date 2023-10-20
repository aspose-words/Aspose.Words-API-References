---
title: TxtSaveOptions.ListIndentation
linktitle: ListIndentation
articleTitle: ListIndentation
second_title: Aspose.Words pour .NET
description: TxtSaveOptions ListIndentation propriété. Obtient unTxtListIndentation objet qui spécifie combien et quel caractère utiliser pour lindentation des niveaux de liste. Par défaut il sagit dun nombre nul de caractères 0 ce qui signifie aucune indentation en C#.
type: docs
weight: 30
url: /fr/net/aspose.words.saving/txtsaveoptions/listindentation/
---
## TxtSaveOptions.ListIndentation property

Obtient un[`TxtListIndentation`](../../txtlistindentation/) objet qui spécifie combien et quel caractère utiliser pour l'indentation des niveaux de liste. Par défaut, il s'agit d'un nombre nul de caractères '\0', ce qui signifie aucune indentation.

```csharp
public TxtListIndentation ListIndentation { get; }
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

* class [TxtListIndentation](../../txtlistindentation/)
* class [TxtSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
