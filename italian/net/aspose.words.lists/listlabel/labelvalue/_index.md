---
title: ListLabel.LabelValue
second_title: Aspose.Words per .NET API Reference
description: ListLabel proprietà. Ottiene un valore numerico per questa etichetta.
type: docs
weight: 30
url: /it/net/aspose.words.lists/listlabel/labelvalue/
---
## ListLabel.LabelValue property

Ottiene un valore numerico per questa etichetta.

```csharp
public int LabelValue { get; }
```

### Osservazioni

Usa il[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) metodo per aggiornare il valore di questa proprietà.

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

* class [ListLabel](../)
* spazio dei nomi [Aspose.Words.Lists](../../listlabel/)
* assemblea [Aspose.Words](../../../)


