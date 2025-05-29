---
title: SdtListItemCollection Class
linktitle: SdtListItemCollection
articleTitle: SdtListItemCollection
second_title: Aspose.Words per .NET
description: Esplora la classe Aspose.Words.Markup.SdtListItemCollection per un accesso senza interruzioni agli elementi SdtListItem, migliorando la gestione strutturata dei documenti senza sforzo.
type: docs
weight: 4720
url: /it/net/aspose.words.markup/sdtlistitemcollection/
---
## SdtListItemCollection class

Fornisce l'accesso a[`SdtListItem`](../sdtlistitem/) elementi di un tag di documento strutturato.

Per saperne di più, visita il[Tag di documenti strutturati o controllo dei contenuti](https://docs.aspose.com/words/net/working-with-content-control-sdt/) articolo di documentazione.

```csharp
public class SdtListItemCollection : IEnumerable<SdtListItem>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.markup/sdtlistitemcollection/count/) { get; } | Ottiene il numero di elementi nella raccolta. |
| [Item](../../aspose.words.markup/sdtlistitemcollection/item/) { get; } | Restituisce un[`SdtListItem`](../sdtlistitem/) oggetto dato il suo indice a base zero nella raccolta. |
| [SelectedValue](../../aspose.words.markup/sdtlistitemcollection/selectedvalue/) { get; set; } | Specifica il valore attualmente selezionato in questo elenco. È consentito un valore nullo, il che significa che nessuna voce attualmente selezionata è associata a questa raccolta di elementi dell'elenco. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words.markup/sdtlistitemcollection/add/)(*[SdtListItem](../sdtlistitem/)*) | Aggiunge un elemento a questa raccolta. |
| [Clear](../../aspose.words.markup/sdtlistitemcollection/clear/)() | Cancella tutti gli elementi da questa raccolta. |
| [GetEnumerator](../../aspose.words.markup/sdtlistitemcollection/getenumerator/)() | Restituisce un oggetto enumeratore che può essere utilizzato per scorrere tutti gli elementi nella raccolta. |
| [RemoveAt](../../aspose.words.markup/sdtlistitemcollection/removeat/)(*int*) | Rimuove un elemento dell'elenco all'indice specificato. |

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

* class [SdtListItem](../sdtlistitem/)
* spazio dei nomi [Aspose.Words.Markup](../../aspose.words.markup/)
* assemblea [Aspose.Words](../../)
