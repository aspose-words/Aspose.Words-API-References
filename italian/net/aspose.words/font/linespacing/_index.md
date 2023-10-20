---
title: Font.LineSpacing
linktitle: LineSpacing
articleTitle: LineSpacing
second_title: Aspose.Words per .NET
description: Font LineSpacing proprietà. Restituisce linterlinea di questo carattere in punti in C#.
type: docs
weight: 190
url: /it/net/aspose.words/font/linespacing/
---
## Font.LineSpacing property

Restituisce l'interlinea di questo carattere (in punti).

```csharp
public double LineSpacing { get; }
```

## Esempi

Mostra come ottenere l'interlinea di un carattere, in punti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Imposta caratteri diversi per DocumentBuilder e verifica la loro interlinea.
builder.Font.Name = "Calibri";
Assert.AreEqual(14.6484375d, builder.Font.LineSpacing);

builder.Font.Name = "Times New Roman";
Assert.AreEqual(13.798828125d, builder.Font.LineSpacing);
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
