---
title: SdtListItemCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words per .NET
description: Rimuovi senza sforzo un elemento di una lista in base all'indice con il metodo RemoveAt di SdtListItemCollection. Semplifica la gestione dei tuoi dati oggi stesso!
type: docs
weight: 70
url: /it/net/aspose.words.markup/sdtlistitemcollection/removeat/
---
## SdtListItemCollection.RemoveAt method

Rimuove un elemento dell'elenco all'indice specificato.

```csharp
public void RemoveAt(int index)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | Int32 | Indice a partire da zero dell'elemento da rimuovere. |

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

* class [SdtListItemCollection](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
