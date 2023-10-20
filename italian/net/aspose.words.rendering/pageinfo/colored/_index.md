---
title: PageInfo.Colored
linktitle: Colored
articleTitle: Colored
second_title: Aspose.Words per .NET
description: PageInfo Colored proprietà. RestituisceVERO se la pagina contiene contenuti colorati in C#.
type: docs
weight: 10
url: /it/net/aspose.words.rendering/pageinfo/colored/
---
## PageInfo.Colored property

Restituisce`VERO` se la pagina contiene contenuti colorati.

```csharp
public bool Colored { get; }
```

## Esempi

Mostra come verificare se la pagina è a colori o meno.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Controlla che la prima pagina del documento non sia colorata.
Assert.IsFalse(doc.GetPageInfo(0).Colored);
```

### Guarda anche

* class [PageInfo](../)
* spazio dei nomi [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* assemblea [Aspose.Words](../../../)
