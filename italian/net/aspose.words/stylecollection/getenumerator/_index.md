---
title: StyleCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words per .NET
description: Scopri il metodo GetEnumerator di StyleCollection per elencare facilmente gli stili in ordine alfabetico per nome. Migliora la tua efficienza di programmazione oggi stesso!
type: docs
weight: 90
url: /it/net/aspose.words/stylecollection/getenumerator/
---
## StyleCollection.GetEnumerator method

Ottiene un oggetto enumeratore che enumererà gli stili in ordine alfabetico in base ai loro nomi.

```csharp
public IEnumerator<Style> GetEnumerator()
```

## Esempi

Mostra come accedere alla raccolta di stili di un documento.

```csharp
Document doc = new Document();

Assert.AreEqual(4, doc.Styles.Count);

// Enumera ed elenca tutti gli stili contenuti per impostazione predefinita in un documento creato utilizzando Aspose.Words.
using (IEnumerator<Style> stylesEnum = doc.Styles.GetEnumerator())
{
    while (stylesEnum.MoveNext())
    {
        Style curStyle = stylesEnum.Current;
        Console.WriteLine($"Style name:\t\"{curStyle.Name}\", of type \"{curStyle.Type}\"");
        Console.WriteLine($"\tSubsequent style:\t{curStyle.NextParagraphStyleName}");
        Console.WriteLine($"\tIs heading:\t\t\t{curStyle.IsHeading}");
        Console.WriteLine($"\tIs QuickStyle:\t\t{curStyle.IsQuickStyle}");

        Assert.AreEqual(doc, curStyle.Document);
    }
}
```

### Guarda anche

* class [Style](../../style/)
* class [StyleCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
