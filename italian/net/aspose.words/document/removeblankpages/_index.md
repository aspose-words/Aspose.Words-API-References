---
title: Document.RemoveBlankPages
linktitle: RemoveBlankPages
articleTitle: RemoveBlankPages
second_title: Aspose.Words per .NET
description: Migliora senza sforzo i tuoi documenti con il metodo RemoveBlankPages, eliminando le pagine vuote indesiderate per una finitura impeccabile e professionale.
type: docs
weight: 700
url: /it/net/aspose.words/document/removeblankpages/
---
## Document.RemoveBlankPages method

Rimuove le pagine vuote dal documento.

```csharp
public List<int> RemoveBlankPages()
```

### Valore di ritorno

L'elenco dei numeri di pagina è stato considerato vuoto e rimosso.

## Osservazioni

Il documento risultante non conterrà pagine considerate vuote, mentre altri contenuti, tra cui numerazione, intestazioni/piè di pagina e layout generale, rimarranno invariati. La pagina è considerata vuota quando il corpo della pagina non ha contenuto visibile, ad esempio, una tabella vuota senza bordi sarà considerata invisibile e quindi la pagina sarà rilevata come vuota.

## Esempi

Mostra come rimuovere le pagine vuote dal documento.

```csharp
Document doc = new Document(MyDir + "Blank pages.docx");
Assert.AreEqual(2, doc.PageCount);
doc.RemoveBlankPages();
doc.UpdatePageLayout();
Assert.AreEqual(1, doc.PageCount);
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
