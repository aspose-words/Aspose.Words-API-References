---
title: Style.BaseStyleName
second_title: Aspose.Words per .NET API Reference
description: Style proprietà. Ottiene/imposta il nome dello stile su cui è basato questo stile.
type: docs
weight: 30
url: /it/net/aspose.words/style/basestylename/
---
## Style.BaseStyleName property

Ottiene/imposta il nome dello stile su cui è basato questo stile.

```csharp
public string BaseStyleName { get; set; }
```

### Osservazioni

Questa sarà una stringa vuota se lo stile non è basato su nessun altro stile e può essere impostata su una stringa vuota.

### Esempi

Mostra come utilizzare gli alias di stile.

```csharp
Document doc = new Document(MyDir + "Style with alias.docx");

// Questo documento contiene uno stile denominato "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
// Se il nome di uno stile ha più valori separati da virgole, ogni clausola è un alias separato.
Style style = doc.Styles["MyStyle"];
Assert.AreEqual(new [] { "MyStyle Alias 1", "MyStyle Alias 2" }, style.Aliases);
Assert.AreEqual("Title", style.BaseStyleName);
Assert.AreEqual("MyStyle Char", style.LinkedStyleName);

// Possiamo fare riferimento a uno stile utilizzando il suo alias e il suo nome.
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
* spazio dei nomi [Aspose.Words](../../style/)
* assemblea [Aspose.Words](../../../)


