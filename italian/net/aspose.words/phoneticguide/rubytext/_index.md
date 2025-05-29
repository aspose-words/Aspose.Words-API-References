---
title: PhoneticGuide.RubyText
linktitle: RubyText
articleTitle: RubyText
second_title: Aspose.Words per .NET
description: Scopri la proprietà PhoneticGuide RubyText per accedere e migliorare il testo Ruby, ottenendo così una maggiore chiarezza fonetica nelle tue applicazioni.
type: docs
weight: 20
url: /it/net/aspose.words/phoneticguide/rubytext/
---
## PhoneticGuide.RubyText property

Ottiene il testo Ruby della guida fonetica.

```csharp
public string RubyText { get; }
```

## Esempi

Mostra come ottenere le proprietà della guida fonetica.

```csharp
Document doc = new Document(MyDir + "Phonetic guide.docx");

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;
// Utilizzare la guida fonetica nel testo asiatico.
Assert.AreEqual(true, runs[0].IsPhoneticGuide);

PhoneticGuide phoneticGuide = runs[0].PhoneticGuide;
Assert.AreEqual("base", phoneticGuide.BaseText);
Assert.AreEqual("ruby", phoneticGuide.RubyText);
```

### Guarda anche

* class [PhoneticGuide](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
