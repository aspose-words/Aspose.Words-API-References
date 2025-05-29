---
title: FileCorruptedException Class
linktitle: FileCorruptedException
articleTitle: FileCorruptedException
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.FileCorruptedException, progettata per gestire senza problemi i documenti corrotti durante il caricamento. Garantisci una gestione impeccabile dei documenti!
type: docs
weight: 3210
url: /it/net/aspose.words/filecorruptedexception/
---
## FileCorruptedException class

Generato durante il caricamento del documento, quando il documento sembra danneggiato e impossibile da caricare.

Per saperne di più, visita il[Programmazione con documenti](https://docs.aspose.com/words/net/programming-with-documents/) articolo di documentazione.

```csharp
public class FileCorruptedException : Exception
```

## Esempi

Mostra come catturare un FileCorruptedException.

```csharp
try
{
    // Se riceviamo un messaggio di errore "Contenuto illeggibile" quando proviamo ad aprire un documento utilizzando Microsoft Word,
    // è probabile che venga generata un'eccezione quando si tenta di caricare quel documento utilizzando Aspose.Words.
    Document doc = new Document(MyDir + "Corrupted document.docx");
}
catch (FileCorruptedException e)
{
    Console.WriteLine(e.Message);
}
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
