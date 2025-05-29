---
title: PageInfo.Colored
linktitle: Colored
articleTitle: Colored
second_title: Aspose.Words per .NET
description: Scopri se la tua pagina presenta contenuti dai colori vivaci con la proprietà PageInfo Colored. Aumenta il coinvolgimento degli utenti e migliora l'aspetto visivo!
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

Mostra come verificare se la pagina è a colori oppure no.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Controlla che la prima pagina del documento non sia colorata.
Assert.IsFalse(doc.GetPageInfo(0).Colored);
```

### Guarda anche

* class [PageInfo](../)
* spazio dei nomi [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* assemblea [Aspose.Words](../../../)
