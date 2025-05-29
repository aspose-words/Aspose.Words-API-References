---
title: PhoneticGuide.RubyText
linktitle: RubyText
articleTitle: RubyText
second_title: Aspose.Words für .NET
description: Entdecken Sie die PhoneticGuide RubyText-Eigenschaft, um auf Ruby-Text zuzugreifen und ihn zu verbessern und so die phonetische Klarheit in Ihren Anwendungen zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words/phoneticguide/rubytext/
---
## PhoneticGuide.RubyText property

Ruft den Ruby-Text des Phonetikführers ab.

```csharp
public string RubyText { get; }
```

## Beispiele

Zeigt, wie man Eigenschaften des Phonetikleitfadens erhält.

```csharp
Document doc = new Document(MyDir + "Phonetic guide.docx");

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;
// Verwenden Sie im asiatischen Text die Phonetikanleitung.
Assert.AreEqual(true, runs[0].IsPhoneticGuide);

PhoneticGuide phoneticGuide = runs[0].PhoneticGuide;
Assert.AreEqual("base", phoneticGuide.BaseText);
Assert.AreEqual("ruby", phoneticGuide.RubyText);
```

### Siehe auch

* class [PhoneticGuide](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
