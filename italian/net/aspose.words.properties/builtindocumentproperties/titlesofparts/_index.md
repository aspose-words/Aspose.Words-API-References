---
title: BuiltInDocumentProperties.TitlesOfParts
linktitle: TitlesOfParts
articleTitle: TitlesOfParts
second_title: Aspose.Words per .NET
description: Scopri la proprietà TitlesOfParts in BuiltInDocumentProperties. Gestisci facilmente le sezioni del documento con nomi di parti chiari e personalizzabili per una migliore organizzazione.
type: docs
weight: 330
url: /it/net/aspose.words.properties/builtindocumentproperties/titlesofparts/
---
## BuiltInDocumentProperties.TitlesOfParts property

Ogni stringa nell'array specifica il nome di una parte nel documento.

```csharp
public string[] TitlesOfParts { get; set; }
```

## Osservazioni

Aspose.Words non aggiorna questa proprietà.

## Esempi

Mostra la relazione tra le proprietà "HeadingPairs" e "TitlesOfParts".

```csharp
Document doc = new Document(MyDir + "Heading pairs and titles of parts.docx");

// Possiamo trovare i valori combinati di queste raccolte tramite
// "File" -> "Proprietà" -> "Proprietà avanzate" -> scheda "Contenuto".
// La proprietà HeadingPairs è una raccolta di coppie <string, int> che
// determina su quante parti del documento si estende un'intestazione.
object[] headingPairs = doc.BuiltInDocumentProperties.HeadingPairs;

// La proprietà TitlesOfParts contiene i nomi delle parti che appartengono alle intestazioni sopra.
string[] titlesOfParts = doc.BuiltInDocumentProperties.TitlesOfParts;

int headingPairsIndex = 0;
int titlesOfPartsIndex = 0;
while (headingPairsIndex < headingPairs.Length)
{
    Console.WriteLine($"Parts for {headingPairs[headingPairsIndex++]}:");
    int partsCount = Convert.ToInt32(headingPairs[headingPairsIndex++]);

    for (int i = 0; i < partsCount; i++)
        Console.WriteLine($"\t\"{titlesOfParts[titlesOfPartsIndex++]}\"");
}
```

### Guarda anche

* class [BuiltInDocumentProperties](../)
* spazio dei nomi [Aspose.Words.Properties](../../../aspose.words.properties/)
* assemblea [Aspose.Words](../../../)
