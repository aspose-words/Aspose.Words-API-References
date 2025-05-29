---
title: BuiltInDocumentProperties.HeadingPairs
linktitle: HeadingPairs
articleTitle: HeadingPairs
second_title: Aspose.Words per .NET
description: Esplora la proprietà HeadingPairs in BuiltInDocumentProperties per gestire facilmente le intestazioni dei documenti e migliorarne l'organizzazione.
type: docs
weight: 110
url: /it/net/aspose.words.properties/builtindocumentproperties/headingpairs/
---
## BuiltInDocumentProperties.HeadingPairs property

Specifica le intestazioni dei documenti e i loro nomi.

```csharp
public object[] HeadingPairs { get; set; }
```

## Osservazioni

Ogni coppia di intestazioni occupa due elementi in questo array.

Il primo elemento della coppia è unString e specifica il nome dell'intestazione. Il secondo elemento della coppia è unInt32 e specifica il conteggio delle parti document per questa intestazione in[`TitlesOfParts`](../titlesofparts/) proprietà.

La somma totale dei conteggi per tutte le coppie di intestazioni in questa proprietà deve essere uguale al numero di elementi in[`TitlesOfParts`](../titlesofparts/) proprietà.

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
