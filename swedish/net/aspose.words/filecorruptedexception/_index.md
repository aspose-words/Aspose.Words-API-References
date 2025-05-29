---
title: FileCorruptedException Class
linktitle: FileCorruptedException
articleTitle: FileCorruptedException
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.FileCorruptedException, utformad för att hantera skadade dokument utan problem under inläsning. Säkerställ sömlös dokumenthantering!
type: docs
weight: 3210
url: /sv/net/aspose.words/filecorruptedexception/
---
## FileCorruptedException class

Kastas under dokumentinläsning, när dokumentet verkar vara skadat och omöjligt att läsa in.

För att lära dig mer, besök[Programmering med dokument](https://docs.aspose.com/words/net/programming-with-documents/) dokumentationsartikel.

```csharp
public class FileCorruptedException : Exception
```

## Exempel

Visar hur man upptäcker ett FileCorruptedException.

```csharp
try
{
    // Om vi får felmeddelandet "Oläsligt innehåll" när vi försöker öppna ett dokument med Microsoft Word,
    // chansen är stor att vi får ett undantag när vi försöker ladda dokumentet med Aspose.Words.
    Document doc = new Document(MyDir + "Corrupted document.docx");
}
catch (FileCorruptedException e)
{
    Console.WriteLine(e.Message);
}
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
