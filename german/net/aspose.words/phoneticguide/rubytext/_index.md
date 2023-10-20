---
title: PhoneticGuide.RubyText
linktitle: RubyText
articleTitle: RubyText
second_title: Aspose.Words für .NET
description: PhoneticGuide RubyText eigendom. Ruft RubyText des phonetischen Leitfadens ab in C#.
type: docs
weight: 20
url: /de/net/aspose.words/phoneticguide/rubytext/
---
## PhoneticGuide.RubyText property

Ruft Ruby-Text des phonetischen Leitfadens ab.

```csharp
public string RubyText { get; }
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

* class [PhoneticGuide](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
