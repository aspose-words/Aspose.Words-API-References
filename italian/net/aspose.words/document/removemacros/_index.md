---
title: Document.RemoveMacros
second_title: Aspose.Words per .NET API Reference
description: Document metodo. Rimuove dal documento tutte le macro il progetto VBA le barre degli strumenti e le personalizzazioni dei comandi.
type: docs
weight: 650
url: /it/net/aspose.words/document/removemacros/
---
## Document.RemoveMacros method

Rimuove dal documento tutte le macro (il progetto VBA), le barre degli strumenti e le personalizzazioni dei comandi.

```csharp
public void RemoveMacros()
```

### Osservazioni

Rimuovendo tutte le macro da un documento è possibile assicurarsi che il documento non contenga virus di macro.

### Esempi

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
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)


