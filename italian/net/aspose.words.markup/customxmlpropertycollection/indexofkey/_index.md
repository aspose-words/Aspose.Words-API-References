---
title: CustomXmlPropertyCollection.IndexOfKey
linktitle: IndexOfKey
articleTitle: IndexOfKey
second_title: Aspose.Words per .NET
description: Scopri il metodo IndexOfKey di CustomXmlPropertyCollection per trovare facilmente l'indice a base zero di qualsiasi proprietà nella tua collezione. Migliora la tua efficienza di programmazione!
type: docs
weight: 70
url: /it/net/aspose.words.markup/customxmlpropertycollection/indexofkey/
---
## CustomXmlPropertyCollection.IndexOfKey method

Restituisce l'indice basato su zero della proprietà specificata nella raccolta.

```csharp
public int IndexOfKey(string name)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | String | Nome della proprietà con distinzione tra maiuscole e minuscole. |

### Valore di ritorno

Indice a base zero. Valore negativo se non trovato.

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

* class [CustomXmlPropertyCollection](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
