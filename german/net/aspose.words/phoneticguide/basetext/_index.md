---
title: PhoneticGuide.BaseText
linktitle: BaseText
articleTitle: BaseText
second_title: Aspose.Words für .NET
description: Entdecken Sie die PhoneticGuide BaseText-Eigenschaft, um einfach auf den Basistext des Phonetic Guides zuzugreifen und ihn zu verbessern und so die Klarheit und Kommunikation zu verbessern.
type: docs
weight: 10
url: /de/net/aspose.words/phoneticguide/basetext/
---
## PhoneticGuide.BaseText property

Ruft den Basistext des Phonetikleitfadens ab.

```csharp
public string BaseText { get; }
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
