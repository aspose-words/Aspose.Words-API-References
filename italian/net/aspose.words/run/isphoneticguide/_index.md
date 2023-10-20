---
title: Run.IsPhoneticGuide
linktitle: IsPhoneticGuide
articleTitle: IsPhoneticGuide
second_title: Aspose.Words per .NET
description: Run IsPhoneticGuide proprietà. Ottiene un valore booleano che indica che lesecuzione è una guida fonetica in C#.
type: docs
weight: 20
url: /it/net/aspose.words/run/isphoneticguide/
---
## Run.IsPhoneticGuide property

Ottiene un valore booleano che indica che l'esecuzione è una guida fonetica.

```csharp
public bool IsPhoneticGuide { get; }
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

* class [Run](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
