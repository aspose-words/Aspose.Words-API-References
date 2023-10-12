---
title: Style.Type
second_title: Aspose.Words per .NET API Reference
description: Style proprietà. Ottiene il tipo di stile paragrafo o carattere.
type: docs
weight: 180
url: /it/net/aspose.words/style/type/
---
## Style.Type property

Ottiene il tipo di stile (paragrafo o carattere).

```csharp
public StyleType Type { get; }
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

* enum [StyleType](../../styletype/)
* class [Style](../)
* spazio dei nomi [Aspose.Words](../../style/)
* assemblea [Aspose.Words](../../../)


