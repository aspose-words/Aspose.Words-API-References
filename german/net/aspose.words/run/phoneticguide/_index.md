---
title: Run.PhoneticGuide
linktitle: PhoneticGuide
articleTitle: PhoneticGuide
second_title: Aspose.Words für .NET
description: Run PhoneticGuide eigendom. Ruft a abPhoneticGuide Objekt in C#.
type: docs
weight: 40
url: /de/net/aspose.words/run/phoneticguide/
---
## Run.PhoneticGuide property

Ruft a ab`PhoneticGuide` Objekt.

```csharp
public PhoneticGuide PhoneticGuide { get; }
```

## Beispiele

Zeigt, wie man Eigenschaften des phonetischen Führers erhält.

```csharp
Document doc = new Document(MyDir + "Phonetic guide.docx");            

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;
// Lautschrift im asiatischen Text verwenden.
Assert.AreEqual(true, runs[0].IsPhoneticGuide);
Assert.AreEqual("base", runs[0].PhoneticGuide.BaseText);
Assert.AreEqual("ruby", runs[0].PhoneticGuide.RubyText);
```

### Siehe auch

* class [PhoneticGuide](../../phoneticguide/)
* class [Run](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
