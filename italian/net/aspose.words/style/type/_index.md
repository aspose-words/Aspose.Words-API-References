---
title: Style.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words per .NET
description: Scopri la proprietà Tipo di stile per accedere e personalizzare senza sforzo gli stili di paragrafo o di carattere, migliorando l'aspetto visivo del tuo documento.
type: docs
weight: 200
url: /it/net/aspose.words/style/type/
---
## Style.Type property

Ottiene il tipo di stile (paragrafo o carattere).

```csharp
public StyleType Type { get; }
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

* enum [StyleType](../../styletype/)
* class [Style](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
