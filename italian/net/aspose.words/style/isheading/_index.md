---
title: Style.IsHeading
linktitle: IsHeading
articleTitle: IsHeading
second_title: Aspose.Words per .NET
description: Scopri la proprietà IsHeading. Identifica facilmente se uno stile è uno stile di intestazione integrato, migliorando la struttura e la leggibilità del tuo documento.
type: docs
weight: 70
url: /it/net/aspose.words/style/isheading/
---
## Style.IsHeading property

Vero quando lo stile è uno degli stili di intestazione predefiniti.

```csharp
public bool IsHeading { get; }
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

* class [Style](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
