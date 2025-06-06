---
title: Style.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words per .NET
description: Scopri la proprietà Nome stile, gestisci e personalizza facilmente i tuoi stili per una maggiore flessibilità di progettazione e un'esperienza utente migliore.
type: docs
weight: 130
url: /it/net/aspose.words/style/name/
---
## Style.Name property

Ottiene o imposta il nome dello stile.

```csharp
public string Name { get; set; }
```

## Osservazioni

Non può essere una stringa vuota.

Se nella collezione esiste già uno stile con questo nome, questo stile lo sovrascriverà. Tutti i nodi interessati faranno riferimento al nuovo stile.

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

Mostra come clonare lo stile di un documento.

```csharp
Document doc = new Document();

// Il metodo AddCopy crea una copia dello stile specificato e
// genera automaticamente un nuovo nome per lo stile, ad esempio "Titolo 1_0".
Style newStyle = doc.Styles.AddCopy(doc.Styles["Heading 1"]);

// Utilizzare la proprietà "Nome" dello stile per modificare il nome identificativo dello stile.
newStyle.Name = "My Heading 1";

// Il nostro documento ora ha due stili identici ma con nomi diversi.
// La modifica delle impostazioni di uno stile non influisce sull'altro.
newStyle.Font.Color = Color.Red;

Assert.AreEqual("My Heading 1", newStyle.Name);
Assert.AreEqual("Heading 1", doc.Styles["Heading 1"].Name);

Assert.AreEqual(doc.Styles["Heading 1"].Type, newStyle.Type);
Assert.AreEqual(doc.Styles["Heading 1"].Font.Name, newStyle.Font.Name);
Assert.AreEqual(doc.Styles["Heading 1"].Font.Size, newStyle.Font.Size);
Assert.AreNotEqual(doc.Styles["Heading 1"].Font.Color, newStyle.Font.Color);
```

### Guarda anche

* class [Style](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
