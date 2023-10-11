---
title: Style.Document
second_title: Aspose.Words per .NET API Reference
description: Style proprietà. Ottiene il documento del proprietario.
type: docs
weight: 50
url: /it/net/aspose.words/style/document/
---
## Style.Document property

Ottiene il documento del proprietario.

```csharp
public DocumentBase Document { get; }
```

### Esempi

Mostra come accedere alla raccolta di stili di un documento.

```csharp
Document doc = new Document();

Assert.AreEqual(4, doc.Styles.Count);

// Enumera ed elenca tutti gli stili che un documento creato utilizzando Aspose.Words contiene per impostazione predefinita.
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

* class [DocumentBase](../../documentbase/)
* class [Style](../)
* spazio dei nomi [Aspose.Words](../../style/)
* assemblea [Aspose.Words](../../../)


