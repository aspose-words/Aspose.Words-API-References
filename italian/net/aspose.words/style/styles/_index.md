---
title: Style.Styles
linktitle: Styles
articleTitle: Styles
second_title: Aspose.Words per .NET
description: Scopri la proprietà Style Styles per accedere a una raccolta curata di stili, che arricchiranno il tuo design con un'estetica unica e coerente.
type: docs
weight: 190
url: /it/net/aspose.words/style/styles/
---
## Style.Styles property

Ottiene la raccolta di stili a cui appartiene questo stile.

```csharp
public StyleCollection Styles { get; }
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

* class [StyleCollection](../../stylecollection/)
* class [Style](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
