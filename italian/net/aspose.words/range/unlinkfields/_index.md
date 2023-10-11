---
title: Range.UnlinkFields
second_title: Aspose.Words per .NET API Reference
description: Range metodo. Scollega i campi in questo intervallo.
type: docs
weight: 110
url: /it/net/aspose.words/range/unlinkfields/
---
## Range.UnlinkFields method

Scollega i campi in questo intervallo.

```csharp
public void UnlinkFields()
```

### Osservazioni

Sostituisce tutti i campi di questo intervallo con i risultati più recenti.

Per scollegare i campi nell'intero documento utilizzare`UnlinkFields`.

### Esempi

Mostra come scollegare tutti i campi in un intervallo.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");

Section newSection = (Section)doc.Sections[0].Clone(true);
doc.Sections.Add(newSection);

doc.Sections[1].Range.UnlinkFields();
```

### Guarda anche

* class [Range](../)
* spazio dei nomi [Aspose.Words](../../range/)
* assemblea [Aspose.Words](../../../)


