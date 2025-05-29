---
title: Run.IsPhoneticGuide
linktitle: IsPhoneticGuide
articleTitle: IsPhoneticGuide
second_title: Aspose.Words für .NET
description: Entdecken Sie IsPhoneticGuide, ein leistungsstarkes Tool, das ermittelt, ob ein Lauf als phonetische Anleitung dient und so die Klarheit und Lesbarkeit Ihres Textes verbessert.
type: docs
weight: 20
url: /de/net/aspose.words/run/isphoneticguide/
---
## Run.IsPhoneticGuide property

Ruft einen booleschen Wert ab, der angibt, ob der Lauf eine phonetische Anleitung ist.

```csharp
public bool IsPhoneticGuide { get; }
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

* class [Run](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
