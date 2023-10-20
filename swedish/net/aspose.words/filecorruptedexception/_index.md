---
title: FileCorruptedException Class
linktitle: FileCorruptedException
articleTitle: FileCorruptedException
second_title: Aspose.Words för .NET
description: Aspose.Words.FileCorruptedException klass. Kastas under dokumentladdning när dokumentet verkar vara skadat och omöjligt att ladda i C#.
type: docs
weight: 2800
url: /sv/net/aspose.words/filecorruptedexception/
---
## FileCorruptedException class

Kastas under dokumentladdning, när dokumentet verkar vara skadat och omöjligt att ladda.

För att lära dig mer, besök[Programmering med dokument](https://docs.aspose.com/words/net/programming-with-documents/) dokumentationsartikel.

```csharp
public class FileCorruptedException : Exception
```

## Exempel

Visar hur man fångar en FileCorruptedException.

```csharp
try
{
    // Om vi får felmeddelandet "Oläsbart innehåll" när vi försöker öppna ett dokument med Microsoft Word,
    // Chansen är stor att vi får ett undantag när vi försöker ladda det dokumentet med Aspose.Words.
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
