---
title: Document.UpdateListLabels
second_title: Aspose.Words per .NET API Reference
description: Document metodo. Aggiorna le etichette dellelenco per tutti gli elementi dellelenco nel documento.
type: docs
weight: 740
url: /it/net/aspose.words/document/updatelistlabels/
---
## Document.UpdateListLabels method

Aggiorna le etichette dell'elenco per tutti gli elementi dell'elenco nel documento.

```csharp
public void UpdateListLabels()
```

### Osservazioni

Questo metodo aggiorna le proprietà dell'etichetta dell'elenco come[`LabelValue`](../../../aspose.words.lists/listlabel/labelvalue/) e [`LabelString`](../../../aspose.words.lists/listlabel/labelstring/)per ciascuno[`ListLabel`](../../paragraph/listlabel/) oggetto nel documento.

Inoltre, questo metodo viene talvolta chiamato in modo implicito durante l'aggiornamento dei campi nel documento. Questo è obbligatorio perché alcuni campi che possono fare riferimento a numeri di elenco (come TOC o REF) richiedono che siano aggiornati.

### Esempi

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

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)


