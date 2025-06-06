---
title: Style.Equals
linktitle: Equals
articleTitle: Equals
second_title: Aspose.Words per .NET
description: Scopri il metodo Style Equals per confrontare gli stili predefiniti. Impara a conoscere gli stili dei paragrafi collegati e successivi per una formattazione e un design più efficienti.
type: docs
weight: 220
url: /it/net/aspose.words/style/equals/
---
## Style.Equals method

Esegue il confronto con lo stile specificato. Gli stili Istd vengono confrontati solo per gli stili incorporati. Gli stili predefiniti non sono inclusi nel confronto. Lo stile base, lo stile collegato e lo stile del paragrafo successivo vengono confrontati ricorsivamente.

```csharp
public bool Equals(Style style)
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
