---
title: Style.Aliases
linktitle: Aliases
articleTitle: Aliases
second_title: Aspose.Words per .NET
description: Scopri facilmente tutti gli alias di stile con la proprietà Alias di Stile. Se non ne esiste nessuno, ricevi un array di stringhe vuoto. Semplifica la gestione degli stili!
type: docs
weight: 10
url: /it/net/aspose.words/style/aliases/
---
## Style.Aliases property

Recupera tutti gli alias di questo stile. Se lo stile non ha alias, viene restituito un array vuoto di stringhe.

```csharp
public string[] Aliases { get; }
```

## Esempi

Mostra come utilizzare gli alias di stile.

```csharp
Document doc = new Document(MyDir + "Style with alias.docx");

// Questo documento contiene uno stile denominato "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
// Se il nome di uno stile ha più valori separati da virgole, ogni clausola è un alias separato.
Style style = doc.Styles["MyStyle"];
Assert.AreEqual(new [] { "MyStyle Alias 1", "MyStyle Alias 2" }, style.Aliases);
Assert.AreEqual("Title", style.BaseStyleName);
Assert.AreEqual("MyStyle Char", style.LinkedStyleName);

// Possiamo fare riferimento a uno stile utilizzando il suo alias e anche il suo nome.
Assert.AreEqual(doc.Styles["MyStyle Alias 1"], doc.Styles["MyStyle Alias 2"]);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.ParagraphFormat.Style = doc.Styles["MyStyle Alias 1"];
builder.Writeln("Hello world!");
builder.ParagraphFormat.Style = doc.Styles["MyStyle Alias 2"];
builder.Write("Hello again!");

Assert.AreEqual(doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.Style, 
    doc.FirstSection.Body.Paragraphs[1].ParagraphFormat.Style);
```

### Guarda anche

* class [Style](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
