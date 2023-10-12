---
title: SdtListItem.DisplayText
second_title: Aspose.Words per .NET API Reference
description: SdtListItem proprietà. Ottiene il testo da visualizzare nel contenuto dellesecuzione al posto diValue contenuto dellattributo per questa voce di elenco.
type: docs
weight: 20
url: /it/net/aspose.words.markup/sdtlistitem/displaytext/
---
## SdtListItem.DisplayText property

Ottiene il testo da visualizzare nel contenuto dell'esecuzione al posto di[`Value`](../value/) contenuto dell'attributo per questa voce di elenco.

```csharp
public string DisplayText { get; }
```

### Osservazioni

Non può essere`nullo` e non può essere una stringa vuota.

### Esempi

Mostra come lavorare con i tag dei documenti strutturati con elenco a discesa.

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

// Aggiunge altri 3 elementi all'elenco. Inizializza questi elementi utilizzando un costruttore diverso dal primo elemento
// per visualizzare stringhe diverse dai rispettivi valori.
listItems.Add(new SdtListItem("Item 2", "Value 2"));
listItems.Add(new SdtListItem("Item 3", "Value 3"));
listItems.Add(new SdtListItem("Item 4", "Value 4"));

Assert.AreEqual(4, listItems.Count);

// L'elenco a discesa visualizza il primo elemento. Assegnare una voce di elenco diversa a "SelectedValue" per visualizzarla.
listItems.SelectedValue = listItems[3];

Assert.AreEqual("Value 4", listItems.SelectedValue.Value);

// Enumera la raccolta e stampa ogni elemento.
using (IEnumerator<SdtListItem> enumerator = listItems.GetEnumerator())
{
    while (enumerator.MoveNext())
        if (enumerator.Current != null)
            Console.WriteLine($"List item: {enumerator.Current.DisplayText}, value: {enumerator.Current.Value}");
}

 // Rimuove l'ultima voce dell'elenco.
listItems.RemoveAt(3);

Assert.AreEqual(3, listItems.Count);

// Poiché il nostro controllo a discesa è impostato per visualizzare l'elemento rimosso per impostazione predefinita, assegnagli un elemento da visualizzare che esiste.
listItems.SelectedValue = listItems[1];

doc.Save(ArtifactsDir + "StructuredDocumentTag.ListItemCollection.docx");

// Utilizza il metodo "Cancella" per svuotare contemporaneamente l'intera raccolta di elementi a discesa.
listItems.Clear();

Assert.AreEqual(0, listItems.Count);
```

### Guarda anche

* class [SdtListItem](../)
* spazio dei nomi [Aspose.Words.Markup](../../sdtlistitem/)
* assemblea [Aspose.Words](../../../)


