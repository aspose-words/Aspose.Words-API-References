---
title: Class SdtListItem
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Markup.SdtListItem classe. Questo elemento specifica una singola voce di elenco allinterno di un genitoreComboBox oDropDownList tag del documento strutturato.
type: docs
weight: 3780
url: /it/net/aspose.words.markup/sdtlistitem/
---
## SdtListItem class

Questo elemento specifica una singola voce di elenco all'interno di un genitoreComboBox oDropDownList tag del documento strutturato.

```csharp
public class SdtListItem
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [SdtListItem](sdtlistitem/#constructor)(string) | Inizializza una nuova istanza di questa classe. |
| [SdtListItem](sdtlistitem/#constructor_1)(string, string) | Inizializza una nuova istanza di questa classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DisplayText](../../aspose.words.markup/sdtlistitem/displaytext/) { get; } | Ottiene il testo da visualizzare nel contenuto dell'esecuzione al posto di[`Value`](./value/) contenuto dell'attributo per questa voce di elenco. |
| [Value](../../aspose.words.markup/sdtlistitem/value/) { get; } | Ottiene il valore di questa voce di elenco. |

### Esempi

Mostra come lavorare con i tag di documenti strutturati con elenco a discesa.

```csharp
Document doc = new Document();
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// Un tag di documento strutturato con elenco a discesa è un modulo che consente all'utente di farlo
// seleziona un'opzione da un elenco facendo clic con il pulsante sinistro del mouse e aprendo il modulo in Microsoft Word.
// La proprietà "ListItems" contiene tutti gli elementi dell'elenco e ogni elemento dell'elenco è un "SdtListItem".
SdtListItemCollection listItems = tag.ListItems;
listItems.Add(new SdtListItem("Value 1"));

Assert.AreEqual(listItems[0].DisplayText, listItems[0].Value);

// Aggiungi altri 3 elementi dell'elenco. Inizializza questi elementi utilizzando un costruttore diverso rispetto al primo elemento
// per visualizzare stringhe diverse dai loro valori.
listItems.Add(new SdtListItem("Item 2", "Value 2"));
listItems.Add(new SdtListItem("Item 3", "Value 3"));
listItems.Add(new SdtListItem("Item 4", "Value 4"));

Assert.AreEqual(4, listItems.Count);

// L'elenco a discesa mostra il primo elemento. Assegna una voce di elenco diversa a "SelectedValue" per visualizzarla.
listItems.SelectedValue = listItems[3];

Assert.AreEqual("Value 4", listItems.SelectedValue.Value);

// Enumera la raccolta e stampa ogni elemento.
using (IEnumerator<SdtListItem> enumerator = listItems.GetEnumerator())
{
    while (enumerator.MoveNext())
        if (enumerator.Current != null)
            Console.WriteLine($"List item: {enumerator.Current.DisplayText}, value: {enumerator.Current.Value}");
}

 // Rimuove l'ultimo elemento dell'elenco.
listItems.RemoveAt(3);

Assert.AreEqual(3, listItems.Count);

// Poiché il nostro controllo a discesa è impostato per visualizzare l'elemento rimosso per impostazione predefinita, assegnagli un elemento da visualizzare che esiste.
listItems.SelectedValue = listItems[1];

doc.Save(ArtifactsDir + "StructuredDocumentTag.ListItemCollection.docx");

// Usa il metodo "Cancella" per svuotare l'intera raccolta di elementi a discesa in una volta.
listItems.Clear();

Assert.AreEqual(0, listItems.Count);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Markup](../../aspose.words.markup/)
* assemblea [Aspose.Words](../../)


