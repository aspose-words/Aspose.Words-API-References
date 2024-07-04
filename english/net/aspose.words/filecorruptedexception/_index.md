---
title: FileCorruptedException Class
linktitle: FileCorruptedException
articleTitle: FileCorruptedException
second_title: Aspose.Words for .NET
description: Aspose.Words.FileCorruptedException class. Thrown during document load when the document appears to be corrupted and impossible to load in C#.
type: docs
weight: 3040
url: /net/aspose.words/filecorruptedexception/
---
## FileCorruptedException class

Thrown during document load, when the document appears to be corrupted and impossible to load.

To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/net/programming-with-documents/) documentation article.

```csharp
public class FileCorruptedException : Exception
```

## Examples

Shows how to catch a FileCorruptedException.

```csharp
try
{
    // If we get an "Unreadable content" error message when trying to open a document using Microsoft Word,
    // chances are that we will get an exception thrown when trying to load that document using Aspose.Words.
    Document doc = new Document(MyDir + "Corrupted document.docx");
}
catch (FileCorruptedException e)
{
    Console.WriteLine(e.Message);
}
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
