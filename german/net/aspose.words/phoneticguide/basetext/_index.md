---
title: PhoneticGuide.BaseText
second_title: Aspose.Words für .NET-API-Referenz
description: PhoneticGuide eigendom. Ruft den Basistext des phonetischen Leitfadens ab.
type: docs
weight: 10
url: /de/net/aspose.words/phoneticguide/basetext/
---
## PhoneticGuide.BaseText property

Ruft den Basistext des phonetischen Leitfadens ab.

```csharp
public string BaseText { get; }
```

### Beispiele

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

* class [PhoneticGuide](../)
* namensraum [Aspose.Words](../../phoneticguide/)
* Montage [Aspose.Words](../../../)


