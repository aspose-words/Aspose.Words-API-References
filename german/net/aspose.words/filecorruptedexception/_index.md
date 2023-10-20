---
title: FileCorruptedException Class
linktitle: FileCorruptedException
articleTitle: FileCorruptedException
second_title: Aspose.Words für .NET
description: Aspose.Words.FileCorruptedException klas. Wird beim Laden des Dokuments ausgelöst wenn das Dokument beschädigt zu sein scheint und nicht geladen werden kann in C#.
type: docs
weight: 2800
url: /de/net/aspose.words/filecorruptedexception/
---
## FileCorruptedException class

Wird beim Laden des Dokuments ausgelöst, wenn das Dokument beschädigt zu sein scheint und nicht geladen werden kann.

Um mehr zu erfahren, besuchen Sie die[Programmieren mit Dokumenten](https://docs.aspose.com/words/net/programming-with-documents/) Dokumentationsartikel.

```csharp
public class FileCorruptedException : Exception
```

## Beispiele

Zeigt, wie eine FileCorruptedException abgefangen wird.

```csharp
try
{
    // Wenn wir beim Versuch, ein Dokument mit Microsoft Word zu öffnen, die Fehlermeldung „Inhalt nicht lesbar“ erhalten,
    // Es besteht die Möglichkeit, dass beim Versuch, dieses Dokument mit Aspose.Words zu laden, eine Ausnahme ausgelöst wird.
    Document doc = new Document(MyDir + "Corrupted document.docx");
}
catch (FileCorruptedException e)
{
    Console.WriteLine(e.Message);
}
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
