---
title: Enum PreferredWidthType
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Tables.PreferredWidthType enum. Specifica lunità di misura per la larghezza preferita di una tabella o cella.
type: docs
weight: 6300
url: /it/net/aspose.words.tables/preferredwidthtype/
---
## PreferredWidthType enumeration

Specifica l'unità di misura per la larghezza preferita di una tabella o cella.

```csharp
public enum PreferredWidthType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Auto | `1` | La larghezza preferita non è specificata. La larghezza effettiva della tabella o della cella viene specificata utilizzando la larghezza esplicita oppure verrà determinata automaticamente dall'algoritmo di layout della tabella quando la tabella viene visualizzata, a seconda dell'impostazione di adattamento automatico della tabella. |
| Percent | `2` | Misura la larghezza dell'elemento corrente utilizzando una percentuale specificata. |
| Points | `3` | Misura la larghezza dell'oggetto corrente utilizzando un numero di punti specificato (1/72 di pollice). |

### Esempi

Mostra come verificare il tipo di larghezza e il valore preferiti di una cella di tabella.

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


