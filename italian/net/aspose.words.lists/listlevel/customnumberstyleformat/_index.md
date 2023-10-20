---
title: ListLevel.CustomNumberStyleFormat
linktitle: CustomNumberStyleFormat
articleTitle: CustomNumberStyleFormat
second_title: Aspose.Words per .NET
description: ListLevel CustomNumberStyleFormat proprietà. Ottiene il formato di stile numero personalizzato per questo livello di elenco. Ad esempio a ç ĝ  in C#.
type: docs
weight: 20
url: /it/net/aspose.words.lists/listlevel/customnumberstyleformat/
---
## ListLevel.CustomNumberStyleFormat property

Ottiene il formato di stile numero personalizzato per questo livello di elenco. Ad esempio: "a, ç, ĝ, ...".

```csharp
public string CustomNumberStyleFormat { get; }
```

## Esempi

Mostra come ottenere il formato di un elenco con lo stile numero personalizzato.

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

ListLevel listLevel = doc.FirstSection.Body.Paragraphs[0].ListFormat.ListLevel;

string customNumberStyleFormat = string.Empty;

if (listLevel.NumberStyle == NumberStyle.Custom)
    customNumberStyleFormat = listLevel.CustomNumberStyleFormat;

Assert.AreEqual("001, 002, 003, ...", customNumberStyleFormat);

// Possiamo ottenere il valore per l'indice specificato dell'elemento dell'elenco.
Assert.AreEqual("iv", ListLevel.GetEffectiveValue(4, NumberStyle.LowercaseRoman, null));
Assert.AreEqual("005", ListLevel.GetEffectiveValue(5, NumberStyle.Custom, customNumberStyleFormat));
```

### Guarda anche

* class [ListLevel](../)
* spazio dei nomi [Aspose.Words.Lists](../../../aspose.words.lists/)
* assemblea [Aspose.Words](../../../)
