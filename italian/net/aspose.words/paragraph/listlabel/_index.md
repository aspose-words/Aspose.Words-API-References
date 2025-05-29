---
title: Paragraph.ListLabel
linktitle: ListLabel
articleTitle: ListLabel
second_title: Aspose.Words per .NET
description: Accedi e formatta la numerazione degli elenchi con la proprietà Paragraph ListLabel. Migliora l'organizzazione e la chiarezza del tuo documento senza sforzo!
type: docs
weight: 160
url: /it/net/aspose.words/paragraph/listlabel/
---
## Paragraph.ListLabel property

Ottiene un`ListLabel`oggetto che fornisce l'accesso al valore di numerazione e formattazione dell'elenco per questo paragrafo.

```csharp
public ListLabel ListLabel { get; }
```

## Esempi

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

* class [ListLabel](../../../aspose.words.lists/listlabel/)
* class [Paragraph](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
