---
title: Class ListLabel
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Lists.ListLabel classe. Definisce le proprietà specifiche di unetichetta di elenco.
type: docs
weight: 3490
url: /it/net/aspose.words.lists/listlabel/
---
## ListLabel class

Definisce le proprietà specifiche di un'etichetta di elenco.

Per saperne di più, visita il[Lavorare con gli elenchi](https://docs.aspose.com/words/net/working-with-lists/) articolo di documentazione.

```csharp
public class ListLabel
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Font](../../aspose.words.lists/listlabel/font/) { get; } | Ottiene il carattere dell'etichetta dell'elenco. |
| [LabelString](../../aspose.words.lists/listlabel/labelstring/) { get; } | Ottiene una rappresentazione di stringa dell'etichetta dell'elenco. |
| [LabelValue](../../aspose.words.lists/listlabel/labelvalue/) { get; } | Ottiene un valore numerico per questa etichetta. |

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

* spazio dei nomi [Aspose.Words.Lists](../../aspose.words.lists/)
* assemblea [Aspose.Words](../../)


