---
title: Class FileCorruptedException
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.FileCorruptedException classe. Lanciato durante il caricamento del documento quando il documento sembra danneggiato e impossibile da caricare.
type: docs
weight: 2800
url: /it/net/aspose.words/filecorruptedexception/
---
## FileCorruptedException class

Lanciato durante il caricamento del documento, quando il documento sembra danneggiato e impossibile da caricare.

Per saperne di più, visita il[Programmazione con documenti](https://docs.aspose.com/words/net/programming-with-documents/) articolo di documentazione.

```csharp
public class FileCorruptedException : Exception
```

### Esempi

Mostra come intercettare una FileCorruptedException.

```csharp
try
{
    // Se riceviamo il messaggio di errore "Contenuto illeggibile" quando proviamo ad aprire un documento utilizzando Microsoft Word,
    // è probabile che venga generata un'eccezione quando si tenta di caricare il documento utilizzando Aspose.Words.
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


