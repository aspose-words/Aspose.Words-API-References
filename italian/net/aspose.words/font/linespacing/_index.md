---
title: Font.LineSpacing
linktitle: LineSpacing
articleTitle: LineSpacing
second_title: Aspose.Words per .NET
description: Scopri la proprietà Font LineSpacing, che fornisce la spaziatura precisa delle linee in punti, migliorando la leggibilità e il design del testo.
type: docs
weight: 190
url: /it/net/aspose.words/font/linespacing/
---
## Font.LineSpacing property

Restituisce la spaziatura delle linee di questo font (in punti).

```csharp
public double LineSpacing { get; }
```

## Esempi

Mostra come ottenere la spaziatura delle linee di un font, in punti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Imposta diversi font per DocumentBuilder e verifica la spaziatura delle righe.
builder.Font.Name = "Calibri";
Assert.AreEqual(14.6484375d, builder.Font.LineSpacing);

builder.Font.Name = "Times New Roman";
Assert.AreEqual(13.798828125d, builder.Font.LineSpacing);
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
