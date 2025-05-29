---
title: Document.RemoveMacros
linktitle: RemoveMacros
articleTitle: RemoveMacros
second_title: Aspose.Words per .NET
description: Rimuovi senza sforzo tutte le macro, le barre degli strumenti e le impostazioni dei comandi personalizzati dal tuo progetto VBA con il metodo Document RemoveMacros per ottenere un documento più pulito.
type: docs
weight: 720
url: /it/net/aspose.words/document/removemacros/
---
## Document.RemoveMacros method

Rimuove tutte le macro (il progetto VBA), nonché le barre degli strumenti e le personalizzazioni dei comandi dal documento.

```csharp
public void RemoveMacros()
```

## Osservazioni

Rimuovendo tutte le macro da un documento è possibile garantire che il documento non contenga virus macro.

## Esempi

Mostra come rimuovere tutte le macro da un documento.

```csharp
Document doc = new Document(MyDir + "Macro.docm");

Assert.IsTrue(doc.HasMacros);
Assert.AreEqual("Project", doc.VbaProject.Name);

// Rimuove il progetto VBA del documento, insieme a tutte le sue macro.
doc.RemoveMacros();

Assert.IsFalse(doc.HasMacros);
Assert.Null(doc.VbaProject);
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
