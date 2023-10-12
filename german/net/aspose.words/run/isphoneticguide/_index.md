---
title: Run.IsPhoneticGuide
second_title: Aspose.Words für .NET-API-Referenz
description: Run eigendom. Ruft einen booleschen Wert ab der angibt ob es sich bei der Ausführung um einen phonetischen Leitfaden handelt.
type: docs
weight: 20
url: /de/net/aspose.words/run/isphoneticguide/
---
## Run.IsPhoneticGuide property

Ruft einen booleschen Wert ab, der angibt, ob es sich bei der Ausführung um einen phonetischen Leitfaden handelt.

```csharp
public bool IsPhoneticGuide { get; }
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

* class [Run](../)
* namensraum [Aspose.Words](../../run/)
* Montage [Aspose.Words](../../../)


