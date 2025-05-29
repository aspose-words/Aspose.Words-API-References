---
title: Style.LinkedStyleName
linktitle: LinkedStyleName
articleTitle: LinkedStyleName
second_title: Aspose.Words per .NET
description: Scopri come definire lo stile della proprietà LinkedStyleName, gestire facilmente gli stili collegati e migliorare il flusso di lavoro di progettazione con un'integrazione perfetta.
type: docs
weight: 90
url: /it/net/aspose.words/style/linkedstylename/
---
## Style.LinkedStyleName property

Ottiene/imposta il nome del[`Style`](../) Collegato a questo. Restituisce una stringa vuota se non ci sono stili collegati.

```csharp
public string LinkedStyleName { get; set; }
```

## Osservazioni

È consentito solo collegare lo stile del paragrafo allo stile del carattere e viceversa.

Impostando LinkedStyleName per lo stile corrente si ottiene automaticamente l'impostazione di LinkedStyleName per lo stile collegato.

Assegnare una stringa vuota equivale a scollegare lo stile precedentemente collegato.

## Esempi

Mostra come collegare gli stili tra loro.

```csharp
Document doc = new Document();

Style styleHeading1 = doc.Styles[StyleIdentifier.Heading1];

Style styleHeading1Char = doc.Styles.Add(StyleType.Character, "Heading 1 Char");
styleHeading1Char.Font.Name = "Verdana";
styleHeading1Char.Font.Bold = true;
styleHeading1Char.Font.Border.LineStyle = LineStyle.Dot;
styleHeading1Char.Font.Border.LineWidth = 15;

styleHeading1.LinkedStyleName = "Heading 1 Char";

Assert.AreEqual("Heading 1 Char", styleHeading1.LinkedStyleName);
Assert.AreEqual("Heading 1", styleHeading1Char.LinkedStyleName);
```

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
