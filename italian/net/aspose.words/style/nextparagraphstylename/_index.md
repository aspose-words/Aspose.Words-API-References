---
title: Style.NextParagraphStyleName
linktitle: NextParagraphStyleName
articleTitle: NextParagraphStyleName
second_title: Aspose.Words per .NET
description: Scopri come utilizzare in modo efficace la proprietà NextParagraphStyleName per automatizzare l'applicazione dello stile ai nuovi paragrafi, migliorando così la formattazione del documento.
type: docs
weight: 140
url: /it/net/aspose.words/style/nextparagraphstylename/
---
## Style.NextParagraphStyleName property

Ottiene/imposta il nome dello stile da applicare automaticamente a un nuovo paragrafo inserito dopo un paragrafo formattato con lo stile specificato.

```csharp
public string NextParagraphStyleName { get; set; }
```

## Osservazioni

Questa proprietà non è utilizzata da Aspose.Words. Lo stile di paragrafo successivo verrà applicato automaticamente solo quando si modifica il documento in MS Word.

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
