---
title: Run.PhoneticGuide
linktitle: PhoneticGuide
articleTitle: PhoneticGuide
second_title: Aspose.Words für .NET
description: Mit PhoneticGuide erhalten Sie eine nahtlose Aussprache. Verbessern Sie Ihre Sprachkenntnisse und Ihre Kommunikation durch personalisierte phonetische Einblicke.
type: docs
weight: 40
url: /de/net/aspose.words/run/phoneticguide/
---
## Run.PhoneticGuide property

Erhält eine`PhoneticGuide` Objekt.

```csharp
public PhoneticGuide PhoneticGuide { get; }
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

* class [PhoneticGuide](../../phoneticguide/)
* class [Run](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
