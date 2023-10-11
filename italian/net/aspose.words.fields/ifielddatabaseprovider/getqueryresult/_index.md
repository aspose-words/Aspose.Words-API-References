---
title: IFieldDatabaseProvider.GetQueryResult
second_title: Aspose.Words per .NET API Reference
description: IFieldDatabaseProvider metodo. Restituisce il risultato della query.
type: docs
weight: 10
url: /it/net/aspose.words.fields/ifielddatabaseprovider/getqueryresult/
---
## IFieldDatabaseProvider.GetQueryResult method

Restituisce il risultato della query.

```csharp
public FieldDatabaseDataTable GetQueryResult(string fileName, string connection, string query, 
    FieldDatabase field)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Il percorso completo e il nome file del database specificato nel campo \d. |
| connection | String | La connessione ai dati specificati nell'opzione di campo \c. |
| query | String | L'insieme di istruzioni SQL che interrogano il database specificato nell'opzione del campo \s. |
| field | FieldDatabase | Il campo è in fase di aggiornamento. |

### Valore di ritorno

IL[`FieldDatabaseDataTable`](../../fielddatabasedatatable/) istanza che dovrebbe essere utilizzata per l'aggiornamento del campo.

### Guarda anche

* class [FieldDatabaseDataTable](../../fielddatabasedatatable/)
* class [FieldDatabase](../../fielddatabase/)
* interface [IFieldDatabaseProvider](../)
* spazio dei nomi [Aspose.Words.Fields](../../ifielddatabaseprovider/)
* assemblea [Aspose.Words](../../../)


