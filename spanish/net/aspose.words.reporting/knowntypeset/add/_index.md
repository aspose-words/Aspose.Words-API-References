---
title: KnownTypeSet.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words para .NET
description: KnownTypeSet Add método. Agrega lo especificadoType objeto al conjunto. LanzaArgumentException en los siguientes casos en C#.
type: docs
weight: 20
url: /es/net/aspose.words.reporting/knowntypeset/add/
---
## KnownTypeSet.Add method

Agrega lo especificadoType objeto al conjunto. LanzaArgumentException en los siguientes casos:

-*type* es`nulo`.

-*type* representa un tipo vacío.

-*type* representa un tipo invisible, es decir, un tipo no público o un tipo anidado público que tiene un tipo externo no público.

-*type* representa un tipo genérico.

-*type* representa un tipo de matriz.

-*type* ya se ha agregado al conjunto.

```csharp
public void Add(Type type)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| type | Type | AType objeto a agregar. |

### Ver también

* class [KnownTypeSet](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)
