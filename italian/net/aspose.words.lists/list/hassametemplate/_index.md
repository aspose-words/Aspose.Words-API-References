---
title: List.HasSameTemplate
linktitle: HasSameTemplate
articleTitle: HasSameTemplate
second_title: Aspose.Words per .NET
description: Scopri il metodo HasSameTemplate, controlla facilmente se due elenchi condividono lo stesso modello, garantendo coerenza ed efficienza nella gestione dei dati.
type: docs
weight: 120
url: /it/net/aspose.words.lists/list/hassametemplate/
---
## List.HasSameTemplate method

Restituisce true se l'elenco corrente e l'elenco specificato vengono creati dallo stesso modello.

```csharp
public bool HasSameTemplate(List other)
```

## Esempi

Mostra come definire elenchi con lo stesso ListDefId.

```csharp
Document doc = new Document(MyDir + "Different lists.docx");

Assert.True(doc.Lists[0].HasSameTemplate(doc.Lists[1]));
Assert.False(doc.Lists[1].HasSameTemplate(doc.Lists[2]));
```

### Guarda anche

* class [List](../)
* spazio dei nomi [Aspose.Words.Lists](../../../aspose.words.lists/)
* assemblea [Aspose.Words](../../../)
