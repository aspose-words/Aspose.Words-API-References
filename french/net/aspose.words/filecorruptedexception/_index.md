---
title: FileCorruptedException Class
linktitle: FileCorruptedException
articleTitle: FileCorruptedException
second_title: Aspose.Words pour .NET
description: Aspose.Words.FileCorruptedException classe. Lancé lors du chargement du document lorsque le document semble corrompu et impossible à charger en C#.
type: docs
weight: 2800
url: /fr/net/aspose.words/filecorruptedexception/
---
## FileCorruptedException class

Lancé lors du chargement du document, lorsque le document semble corrompu et impossible à charger.

Pour en savoir plus, visitez le[Programmation avec des documents](https://docs.aspose.com/words/net/programming-with-documents/) article documentaire.

```csharp
public class FileCorruptedException : Exception
```

## Exemples

Montre comment intercepter une exception FileCorruptedException.

```csharp
try
{
    // Si nous obtenons un message d'erreur "Contenu illisible" lorsque nous essayons d'ouvrir un document avec Microsoft Word,
    // Il y a de fortes chances que nous obtenions une exception levée lors de la tentative de chargement de ce document à l'aide d'Aspose.Words.
    Document doc = new Document(MyDir + "Corrupted document.docx");
}
catch (FileCorruptedException e)
{
    Console.WriteLine(e.Message);
}
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
