---
title: List.HasSameTemplate
linktitle: HasSameTemplate
articleTitle: HasSameTemplate
second_title: Aspose.Words per .NET
description: List HasSameTemplate metodo. Restituisce vero se lelenco corrente e lelenco specificato vengono creati dallo stesso modello in C#.
type: docs
weight: 120
url: /it/net/aspose.words.lists/list/hassametemplate/
---
## List.HasSameTemplate method

Restituisce vero se l'elenco corrente e l'elenco specificato vengono creati dallo stesso modello.

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
