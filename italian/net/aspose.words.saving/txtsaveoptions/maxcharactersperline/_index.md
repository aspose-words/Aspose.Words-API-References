---
title: TxtSaveOptions.MaxCharactersPerLine
linktitle: MaxCharactersPerLine
articleTitle: MaxCharactersPerLine
second_title: Aspose.Words per .NET
description: TxtSaveOptions MaxCharactersPerLine proprietà. Ottiene o imposta un valore intero che specifica il numero massimo di caratteri per riga. Il valore predefinito è 0 ciò significa nessun limite in C#.
type: docs
weight: 40
url: /it/net/aspose.words.saving/txtsaveoptions/maxcharactersperline/
---
## TxtSaveOptions.MaxCharactersPerLine property

Ottiene o imposta un valore intero che specifica il numero massimo di caratteri per riga. Il valore predefinito è 0, ciò significa nessun limite.

```csharp
public int MaxCharactersPerLine { get; set; }
```

## Esempi

Mostra come impostare il numero massimo di caratteri per riga.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Imposta 30 caratteri come massimo consentito per una riga.
TxtSaveOptions saveOptions = new TxtSaveOptions { MaxCharactersPerLine = 30 };

doc.Save(ArtifactsDir + "TxtSaveOptions.MaxCharactersPerLine.txt", saveOptions);
```

### Guarda anche

* class [TxtSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
