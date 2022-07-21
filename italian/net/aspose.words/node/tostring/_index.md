---
title: ToString
second_title: Aspose.Words per .NET API Reference
description: Esporta il contenuto del nodo in una stringa nel formato specificato.
type: docs
weight: 160
url: /it/net/aspose.words/node/tostring/
---
## ToString(SaveFormat) {#tostring_1}

Esporta il contenuto del nodo in una stringa nel formato specificato.

```csharp
public string ToString(SaveFormat saveFormat)
```

### Valore di ritorno

Il contenuto del nodo nel formato specificato.

### Esempi

Mostra la differenza tra la chiamata dei metodi GetText e ToString su un nodo.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// GetText recupererà il testo visibile, codici di campo e caratteri speciali.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015\u000c", doc.GetText());

// ToString ci darà l'aspetto del documento se salvato in un formato di salvataggio passato.
Assert.AreEqual("«Field»\r\n", doc.ToString(SaveFormat.Text));
```

Esporta il contenuto di un nodo in String in formato HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// Quando chiamiamo il metodo ToString usando l'overload di html SaveFormat,
// converte i contenuti del nodo nella loro rappresentazione html grezza.
Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(SaveFormat.Html));

// Possiamo anche modificare il risultato di questa conversione usando un oggetto SaveOptions.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ExportRelativeFontSize = true;

Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(saveOptions));
```

Mostra come estrarre le etichette dell'elenco di tutti i paragrafi che sono elementi dell'elenco.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

// Trova se abbiamo l'elenco dei paragrafi. Nel nostro documento, il nostro elenco utilizza semplici numeri arabi,
// che iniziano alle tre e finiscono alle sei.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // Questo è il testo che otteniamo quando otteniamo quando emettiamo questo nodo in formato testo.
    // Questo output di testo ometterà le etichette dell'elenco. Taglia i caratteri di formattazione del paragrafo. 
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // Ottiene la posizione del paragrafo nel livello corrente dell'elenco. Se abbiamo una lista con più livelli,
    // questo ci dirà quale posizione si trova a quel livello.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // Combinali insieme per includere l'etichetta dell'elenco con il testo nell'output.
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### Guarda anche

* enum [SaveFormat](../../saveformat)
* class [Node](../../node)
* spazio dei nomi [Aspose.Words](../../node)
* assemblea [Aspose.Words](../../../)

---

## ToString(SaveOptions) {#tostring_2}

Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate.

```csharp
public string ToString(SaveOptions saveOptions)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| saveOptions | SaveOptions | Specifica le opzioni che controllano la modalità di salvataggio del nodo. |

### Valore di ritorno

Il contenuto del nodo nel formato specificato.

### Esempi

Esporta il contenuto di un nodo in String in formato HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// Quando chiamiamo il metodo ToString usando l'overload di html SaveFormat,
// converte i contenuti del nodo nella loro rappresentazione html grezza.
Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(SaveFormat.Html));

// Possiamo anche modificare il risultato di questa conversione usando un oggetto SaveOptions.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ExportRelativeFontSize = true;

Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(saveOptions));
```

### Guarda anche

* class [SaveOptions](../../../aspose.words.saving/saveoptions)
* class [Node](../../node)
* spazio dei nomi [Aspose.Words](../../node)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
