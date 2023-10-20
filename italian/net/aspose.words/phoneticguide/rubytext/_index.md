---
title: PhoneticGuide.RubyText
linktitle: RubyText
articleTitle: RubyText
second_title: Aspose.Words per .NET
description: PhoneticGuide RubyText proprietà. Ottiene il testo in rubino della guida fonetica in C#.
type: docs
weight: 20
url: /it/net/aspose.words/phoneticguide/rubytext/
---
## PhoneticGuide.RubyText property

Ottiene il testo in rubino della guida fonetica.

```csharp
public string RubyText { get; }
```

## Esempi

Mostra come ottenere le proprietà della guida fonetica.

```csharp
Document doc = new Document(MyDir + "Phonetic guide.docx");            

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;
// Utilizza la guida fonetica nel testo asiatico.
Assert.AreEqual(true, runs[0].IsPhoneticGuide);
Assert.AreEqual("base", runs[0].PhoneticGuide.BaseText);
Assert.AreEqual("ruby", runs[0].PhoneticGuide.RubyText);
```

### Guarda anche

* class [PhoneticGuide](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
