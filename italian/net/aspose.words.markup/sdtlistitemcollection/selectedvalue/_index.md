---
title: SdtListItemCollection.SelectedValue
linktitle: SelectedValue
articleTitle: SelectedValue
second_title: Aspose.Words per .NET
description: Scopri la proprietà SelectedValue di SdtListItemCollection, che definisce la selezione corrente nell'elenco, consentendo il valore null in caso di nessuna selezione. Migliora la tua gestione dei dati!
type: docs
weight: 30
url: /it/net/aspose.words.markup/sdtlistitemcollection/selectedvalue/
---
## SdtListItemCollection.SelectedValue property

Specifica il valore attualmente selezionato in questo elenco. È consentito un valore nullo, il che significa che nessuna voce attualmente selezionata è associata a questa raccolta di elementi dell'elenco.

```csharp
public SdtListItem SelectedValue { get; set; }
```

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

* class [SdtListItem](../../sdtlistitem/)
* class [SdtListItemCollection](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
