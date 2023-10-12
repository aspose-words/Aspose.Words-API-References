---
title: KnownTypeSet.Add
second_title: Aspose.Words per .NET API Reference
description: KnownTypeSet metodo. Aggiunge quanto specificatoType oggetto dellinsieme. LanciaArgumentException in i seguenti casi
type: docs
weight: 20
url: /it/net/aspose.words.reporting/knowntypeset/add/
---
## KnownTypeSet.Add method

Aggiunge quanto specificatoType oggetto dell'insieme. LanciaArgumentException in i seguenti casi:

-*type* È`nullo`.

-*type* rappresenta un tipo vuoto.

-*type* rappresenta un tipo invisibile, ovvero un tipo non pubblico o un tipo annidato pubblico che ha un tipo esterno non pubblico.

-*type* rappresenta un tipo generico.

-*type* rappresenta un tipo di array.

-*type* è già stato aggiunto al set.

```csharp
public void Add(Type type)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| type | Type | UNType oggetto da aggiungere. |

### Guarda anche

* class [KnownTypeSet](../)
* spazio dei nomi [Aspose.Words.Reporting](../../knowntypeset/)
* assemblea [Aspose.Words](../../../)


