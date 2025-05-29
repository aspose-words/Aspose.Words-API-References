---
title: FileCorruptedException Class
linktitle: FileCorruptedException
articleTitle: FileCorruptedException
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.FileCorruptedException, conçue pour gérer facilement les documents corrompus lors du chargement. Assurez une gestion fluide de vos documents !
type: docs
weight: 3210
url: /fr/net/aspose.words/filecorruptedexception/
---
## FileCorruptedException class

Lancé pendant le chargement du document, lorsque le document semble corrompu et impossible à charger.

Pour en savoir plus, visitez le[Programmation avec des documents](https://docs.aspose.com/words/net/programming-with-documents/) article de documentation.

```csharp
public class FileCorruptedException : Exception
```

## Exemples

Montre comment intercepter une FileCorruptedException.

```csharp
try
{
    // Si nous obtenons un message d'erreur « Contenu illisible » lorsque nous essayons d'ouvrir un document à l'aide de Microsoft Word,
    // il y a de fortes chances que nous obtenions une exception levée lorsque nous essayons de charger ce document à l'aide d'Aspose.Words.
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
