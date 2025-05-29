---
title: SdtListItem Class
linktitle: SdtListItem
articleTitle: SdtListItem
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Markup.SdtListItem, progettata per una gestione efficiente degli elementi di elenco nei documenti strutturati ComboBox e DropDownList.
type: docs
weight: 4710
url: /it/net/aspose.words.markup/sdtlistitem/
---
## SdtListItem class

Questo elemento specifica un singolo elemento di elenco all'interno di un elemento padreComboBox ODropDownList tag documento strutturato.

Per saperne di più, visita il[Tag di documenti strutturati o controllo dei contenuti](https://docs.aspose.com/words/net/working-with-content-control-sdt/) articolo di documentazione.

```csharp
public class SdtListItem
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [SdtListItem](sdtlistitem/#constructor)(*string*) | Inizializza una nuova istanza di questa classe. |
| [SdtListItem](sdtlistitem/#constructor_1)(*string, string*) | Inizializza una nuova istanza di questa classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DisplayText](../../aspose.words.markup/sdtlistitem/displaytext/) { get; } | Ottiene il testo da visualizzare nel contenuto dell'esecuzione al posto di[`Value`](./value/) contenuto degli attributi per questa voce di elenco. |
| [Value](../../aspose.words.markup/sdtlistitem/value/) { get; } | Ottiene il valore di questo elemento dell'elenco. |

## Esempi

Mostra come lavorare con i tag dei documenti strutturati con elenco a discesa.

```csharp
Document doc = new Document();
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// Un tag di documento strutturato con elenco a discesa è un modulo che consente all'utente di
// selezionare un'opzione da un elenco facendo clic con il pulsante sinistro del mouse e aprendo il modulo in Microsoft Word.
// La proprietà "ListItems" contiene tutti gli elementi dell'elenco e ogni elemento dell'elenco è un "SdtListItem".
SdtListItemCollection listItems = tag.ListItems;
listItems.Add(new SdtListItem("Value 1"));

Assert.AreEqual(listItems[0].DisplayText, listItems[0].Value);

// Aggiungi altri 3 elementi all'elenco. Inizializza questi elementi utilizzando un costruttore diverso dal primo elemento.
// per visualizzare stringhe diverse dai loro valori.
listItems.Add(new SdtListItem("Item 2", "Value 2"));
listItems.Add(new SdtListItem("Item 3", "Value 3"));
listItems.Add(new SdtListItem("Item 4", "Value 4"));

Assert.AreEqual(4, listItems.Count);

// L'elenco a discesa mostra il primo elemento. Assegna un elemento diverso a "SelectedValue" per visualizzarlo.
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

// Poiché il nostro controllo a discesa è impostato per visualizzare l'elemento rimosso per impostazione predefinita, assegnagli un elemento da visualizzare che esista.
listItems.SelectedValue = listItems[1];

doc.Save(ArtifactsDir + "StructuredDocumentTag.ListItemCollection.docx");

// Utilizzare il metodo "Clear" per svuotare in una volta sola l'intera raccolta di elementi a discesa.
listItems.Clear();

Assert.AreEqual(0, listItems.Count);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Markup](../../aspose.words.markup/)
* assemblea [Aspose.Words](../../)
