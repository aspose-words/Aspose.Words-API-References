---
title: PreferredWidthType Enum
linktitle: PreferredWidthType
articleTitle: PreferredWidthType
second_title: Aspose.Words per .NET
description: Scopri l'enumerazione Aspose.Words.Tables.PreferredWidthType. Definisci facilmente le misure di larghezza di tabelle e celle per una formattazione precisa dei documenti.
type: docs
weight: 7150
url: /it/net/aspose.words.tables/preferredwidthtype/
---
## PreferredWidthType enumeration

Specifica l'unità di misura per la larghezza preferita di una tabella o di una cella.

```csharp
public enum PreferredWidthType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Auto | `1` | La larghezza preferita non è specificata. La larghezza effettiva della tabella o della cella viene specificata utilizzando la larghezza esplicita oppure verrà determinata automaticamente dall'algoritmo di layout della tabella quando la tabella viene visualizzata, a seconda dell'impostazione di adattamento automatico della tabella. |
| Percent | `2` | Misura la larghezza dell'elemento corrente utilizzando una percentuale specificata. |
| Points | `3` | Misura la larghezza dell'elemento corrente utilizzando un numero specificato di punti (1/72 di pollice). |

## Esempi

Mostra come verificare il tipo di larghezza preferito e il valore di una cella di una tabella.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

Assert.AreEqual(PreferredWidthType.Percent, firstCell.CellFormat.PreferredWidth.Type);
Assert.AreEqual(11.16d, firstCell.CellFormat.PreferredWidth.Value);
```

### Guarda anche

* class [PreferredWidth](../preferredwidth/)
* spazio dei nomi [Aspose.Words.Tables](../../aspose.words.tables/)
* assemblea [Aspose.Words](../../)
