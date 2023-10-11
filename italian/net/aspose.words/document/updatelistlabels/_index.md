---
title: Document.UpdateListLabels
second_title: Aspose.Words per .NET API Reference
description: Document metodo. Aggiorna le etichette dellelenco per tutti gli elementi dellelenco nel documento.
type: docs
weight: 780
url: /it/net/aspose.words/document/updatelistlabels/
---
## Document.UpdateListLabels method

Aggiorna le etichette dell'elenco per tutti gli elementi dell'elenco nel documento.

```csharp
public void UpdateListLabels()
```

### Osservazioni

Questo metodo aggiorna le proprietà dell'etichetta dell'elenco come[`LabelValue`](../../../aspose.words.lists/listlabel/labelvalue/) e [`LabelString`](../../../aspose.words.lists/listlabel/labelstring/) per ciascuno[`ListLabel`](../../paragraph/listlabel/)oggetto nel documento.

Inoltre, questo metodo a volte viene chiamato implicitamente durante l'aggiornamento dei campi nel documento. Questo è obbligatorio perché alcuni campi che possono fare riferimento a numeri di elenco (come TOC o REF) necessitano che siano aggiornati.

### Esempi

Mostra come estrarre le etichette dell'elenco di tutti i paragrafi che sono elementi dell'elenco.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

// Trova se abbiamo l'elenco dei paragrafi. Nel nostro documento, l'elenco utilizza semplici numeri arabi,
// che inizia alle tre e finisce alle sei.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // Questo è il testo che otteniamo quando restituiamo questo nodo in formato testo.
     // Questo output di testo ometterà le etichette dell'elenco. Taglia eventuali caratteri di formattazione del paragrafo.
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // Questo ottiene la posizione del paragrafo nel livello corrente dell'elenco. Se abbiamo un elenco con più livelli,
    // questo ci dirà quale posizione è su quel livello.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // Combinali insieme per includere l'etichetta dell'elenco con il testo nell'output.
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)


