---
title: Style.IsQuickStyle
linktitle: IsQuickStyle
articleTitle: IsQuickStyle
second_title: Aspose.Words per .NET
description: Scopri come la proprietà IsQuickStyle migliora la tua esperienza con MS Word mostrando gli stili nella galleria Stili rapidi per un facile accesso e un flusso di lavoro migliorato.
type: docs
weight: 80
url: /it/net/aspose.words/style/isquickstyle/
---
## Style.IsQuickStyle property

Specifica se questo stile viene visualizzato nella raccolta Stili rapidi all'interno dell'interfaccia utente di MS Word.

```csharp
public bool IsQuickStyle { get; set; }
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
