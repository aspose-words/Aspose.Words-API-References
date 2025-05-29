---
title: Document.UpdateListLabels
linktitle: UpdateListLabels
articleTitle: UpdateListLabels
second_title: Aspose.Words per .NET
description: Aggiorna senza sforzo tutte le etichette delle voci di elenco nel tuo documento con il metodo UpdateListLabels, assicurando coerenza e chiarezza nei tuoi contenuti.
type: docs
weight: 820
url: /it/net/aspose.words/document/updatelistlabels/
---
## Document.UpdateListLabels method

Aggiorna le etichette degli elenchi per tutti gli elementi degli elenchi nel documento.

```csharp
public void UpdateListLabels()
```

## Osservazioni

Questo metodo aggiorna le proprietà dell'etichetta dell'elenco come[`LabelValue`](../../../aspose.words.lists/listlabel/labelvalue/) e [`LabelString`](../../../aspose.words.lists/listlabel/labelstring/) per ciascuno[`ListLabel`](../../paragraph/listlabel/) oggetto nel documento.

Inoltre, questo metodo viene talvolta chiamato implicitamente durante l'aggiornamento dei campi nel documento. Questo è required perché alcuni campi che potrebbero fare riferimento a numeri di elenco (come TOC o REF) devono essere aggiornati.

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

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
