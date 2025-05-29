---
title: CustomXmlPropertyCollection Class
linktitle: CustomXmlPropertyCollection
articleTitle: CustomXmlPropertyCollection
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.Markup.CustomXmlPropertyCollection, un potente strumento per gestire in modo efficiente gli attributi XML personalizzati e le proprietà degli smart tag.
type: docs
weight: 4640
url: /it/net/aspose.words.markup/customxmlpropertycollection/
---
## CustomXmlPropertyCollection class

Rappresenta una raccolta di attributi XML personalizzati o proprietà di tag intelligenti.

Per saperne di più, visita il[Tag di documenti strutturati o controllo dei contenuti](https://docs.aspose.com/words/net/working-with-content-control-sdt/) articolo di documentazione.

```csharp
public class CustomXmlPropertyCollection : IEnumerable<CustomXmlProperty>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlpropertycollection/count/) { get; } | Ottiene il numero di elementi contenuti nella raccolta. |
| [Item](../../aspose.words.markup/customxmlpropertycollection/item/) { get; } | Ottiene una proprietà con il nome specificato. (2 indexers) |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlpropertycollection/add/)(*[CustomXmlProperty](../customxmlproperty/)*) | Aggiunge una proprietà alla raccolta. |
| [Clear](../../aspose.words.markup/customxmlpropertycollection/clear/)() | Rimuove tutti gli elementi dalla raccolta. |
| [Contains](../../aspose.words.markup/customxmlpropertycollection/contains/)(*string*) | Determina se la raccolta contiene una proprietà con il nome specificato. |
| [GetEnumerator](../../aspose.words.markup/customxmlpropertycollection/getenumerator/)() | Restituisce un oggetto enumeratore che può essere utilizzato per scorrere tutti gli elementi nella raccolta. |
| [IndexOfKey](../../aspose.words.markup/customxmlpropertycollection/indexofkey/)(*string*) | Restituisce l'indice basato su zero della proprietà specificata nella raccolta. |
| [Remove](../../aspose.words.markup/customxmlpropertycollection/remove/)(*string*) | Rimuove una proprietà con il nome specificato dalla raccolta. |
| [RemoveAt](../../aspose.words.markup/customxmlpropertycollection/removeat/)(*int*) | Rimuove una proprietà all'indice specificato. |

## Osservazioni

Gli articoli sono[`CustomXmlProperty`](../customxmlproperty/) oggetti.

## Esempi

Mostra come utilizzare le proprietà degli smart tag per ottenere informazioni dettagliate sugli smart tag.

```csharp
Document doc = new Document(MyDir + "Smart tags.doc");

// Un tag intelligente appare in un documento con Microsoft Word che riconosce una parte del suo testo come una qualche forma di dati,
// come un nome, una data o un indirizzo e lo converte in un collegamento ipertestuale che presenta una sottolineatura tratteggiata viola.
// In Word 2003, possiamo abilitare gli smart tag tramite "Strumenti" -> "Opzioni correzione automatica..." -> "Smart Tag".
// Nel nostro documento di input ci sono tre oggetti che Microsoft Word ha registrato come smart tag.
// Gli smart tag possono essere annidati, quindi questa raccolta ne contiene di più.
SmartTag[] smartTags = doc.GetChildNodes(NodeType.SmartTag, true).OfType<SmartTag>().ToArray();

Assert.AreEqual(8, smartTags.Length);

// Il membro "Proprietà" di uno smart tag contiene i suoi metadati, che saranno diversi per ogni tipo di smart tag.
// Le proprietà di uno smart tag di tipo "date" contengono anno, mese e giorno.
CustomXmlPropertyCollection properties = smartTags[7].Properties;

Assert.AreEqual(4, properties.Count);

using (IEnumerator<CustomXmlProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"Property name: {enumerator.Current.Name}, value: {enumerator.Current.Value}");
        Assert.AreEqual("", enumerator.Current.Uri);
    }
}

// Possiamo accedere alle proprietà anche in altri modi, ad esempio tramite una coppia chiave-valore.
Assert.True(properties.Contains("Day"));
Assert.AreEqual("22", properties["Day"].Value);
Assert.AreEqual("2003", properties[2].Value);
Assert.AreEqual(1, properties.IndexOfKey("Month"));

// Di seguito sono riportati tre metodi per rimuovere elementi dalla raccolta delle proprietà.
// 1 - Rimuovi per indice:
properties.RemoveAt(3);

Assert.AreEqual(3, properties.Count);

// 2 - Rimuovi per nome:
properties.Remove("Year");

Assert.AreEqual(2, properties.Count);

// 3 - Cancella l'intera collezione in una volta sola:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Guarda anche

* class [CustomXmlProperty](../customxmlproperty/)
* spazio dei nomi [Aspose.Words.Markup](../../aspose.words.markup/)
* assemblea [Aspose.Words](../../)
