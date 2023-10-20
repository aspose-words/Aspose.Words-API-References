---
title: SdtListItemCollection Class
linktitle: SdtListItemCollection
articleTitle: SdtListItemCollection
second_title: Aspose.Words per .NET
description: Aspose.Words.Markup.SdtListItemCollection classe. Fornisce laccesso aSdtListItem elementi di un tag di documento strutturato in C#.
type: docs
weight: 4030
url: /it/net/aspose.words.markup/sdtlistitemcollection/
---
## SdtListItemCollection class

Fornisce l'accesso a[`SdtListItem`](../sdtlistitem/) elementi di un tag di documento strutturato.

Per saperne di più, visita il[Tag di documenti strutturati o controllo del contenuto](https://docs.aspose.com/words/net/working-with-content-control-sdt/) articolo di documentazione.

```csharp
public class SdtListItemCollection : IEnumerable<SdtListItem>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.markup/sdtlistitemcollection/count/) { get; } | Ottiene il numero di elementi nella raccolta. |
| [Item](../../aspose.words.markup/sdtlistitemcollection/item/) { get; } | Restituisce a[`SdtListItem`](../sdtlistitem/) oggetto dato il suo indice in base zero nella raccolta. |
| [SelectedValue](../../aspose.words.markup/sdtlistitemcollection/selectedvalue/) { get; set; } | Specifica il valore attualmente selezionato in questo elenco. È consentito un valore nullo, il che significa che nessuna voce attualmente selezionata è associata a questa raccolta di elementi dell'elenco. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words.markup/sdtlistitemcollection/add/)(*[SdtListItem](../sdtlistitem/)*) | Aggiunge un elemento a questa raccolta. |
| [Clear](../../aspose.words.markup/sdtlistitemcollection/clear/)() | Cancella tutti gli elementi da questa raccolta. |
| [GetEnumerator](../../aspose.words.markup/sdtlistitemcollection/getenumerator/)() | Restituisce un oggetto enumeratore che può essere utilizzato per scorrere tutti gli elementi della raccolta. |
| [RemoveAt](../../aspose.words.markup/sdtlistitemcollection/removeat/)(*int*) | Rimuove una voce di elenco nell'indice specificato. |

## Esempi

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

* class [SdtListItem](../sdtlistitem/)
* spazio dei nomi [Aspose.Words.Markup](../../aspose.words.markup/)
* assemblea [Aspose.Words](../../)
