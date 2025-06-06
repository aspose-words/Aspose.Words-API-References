---
title: Node.ToString
linktitle: ToString
articleTitle: ToString
second_title: Aspose.Words per .NET
description: Scopri il metodo Node ToString e converti facilmente il contenuto dei nodi in stringhe con formati personalizzabili per una migliore gestione dei dati. Ottimizza il tuo codice oggi stesso!
type: docs
weight: 160
url: /it/net/aspose.words/node/tostring/
---
## ToString(*[SaveFormat](../../saveformat/)*) {#tostring_1}

Esporta il contenuto del nodo in una stringa nel formato specificato.

```csharp
public string ToString(SaveFormat saveFormat)
```

### Valore di ritorno

Il contenuto del nodo nel formato specificato.

## Esempi

Mostra la differenza tra la chiamata dei metodi GetText e ToString su un nodo.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// GetText recupererà il testo visibile, nonché i codici di campo e i caratteri speciali.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015", doc.GetText().Trim());

// ToString ci fornirà l'aspetto del documento se salvato in un formato di salvataggio trasmesso.
Assert.AreEqual("«Field»", doc.ToString(SaveFormat.Text).Trim());
```

Esporta il contenuto di un nodo in formato String in formato HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// Quando chiamiamo il metodo ToString utilizzando il sovraccarico html SaveFormat,
// converte il contenuto del nodo nella sua rappresentazione HTML grezza.
Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(SaveFormat.Html));

// Possiamo anche modificare il risultato di questa conversione utilizzando un oggetto SaveOptions.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ExportRelativeFontSize = true;

Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(saveOptions));
```

Mostra come estrarre le etichette di elenco di tutti i paragrafi che sono elementi di elenco.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

// Verifica se abbiamo l'elenco dei paragrafi. Nel nostro documento, l'elenco utilizza numeri arabi semplici,
// che iniziano alle tre e finiscono alle sei.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem).ToList())
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // Questo è il testo che otteniamo quando convertiamo questo nodo in formato testo.
     // Questo output di testo ometterà le etichette degli elenchi. Eliminare eventuali caratteri di formattazione del paragrafo.
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // Questo ottiene la posizione del paragrafo nel livello corrente dell'elenco. Se abbiamo un elenco con più livelli,
    // questo ci dirà quale posizione si trova a quel livello.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // Combinali insieme per includere l'etichetta dell'elenco con il testo nell'output.
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### Guarda anche

* enum [SaveFormat](../../saveformat/)
* class [Node](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## ToString(*[SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#tostring_2}

Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate.

```csharp
public string ToString(SaveOptions saveOptions)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| saveOptions | SaveOptions | Specifica le opzioni che controllano la modalità di salvataggio del nodo. |

### Valore di ritorno

Il contenuto del nodo nel formato specificato.

## Esempi

Esporta il contenuto di un nodo in formato String in formato HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// Quando chiamiamo il metodo ToString utilizzando il sovraccarico html SaveFormat,
// converte il contenuto del nodo nella sua rappresentazione HTML grezza.
Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(SaveFormat.Html));

// Possiamo anche modificare il risultato di questa conversione utilizzando un oggetto SaveOptions.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ExportRelativeFontSize = true;

Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(saveOptions));
```

### Guarda anche

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Node](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
