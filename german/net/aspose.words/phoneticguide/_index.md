---
title: PhoneticGuide Class
linktitle: PhoneticGuide
articleTitle: PhoneticGuide
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.PhoneticGuide zur Verbesserung der Textlesbarkeit mit phonetischen Hilfslinien. Verbessern Sie mühelos Benutzerfreundlichkeit und Zugänglichkeit!
type: docs
weight: 5160
url: /de/net/aspose.words/phoneticguide/
---
## PhoneticGuide class

Steht für Phonetic Guide.

```csharp
public class PhoneticGuide
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BaseText](../../aspose.words/phoneticguide/basetext/) { get; } | Ruft den Basistext des Phonetikleitfadens ab. |
| [RubyText](../../aspose.words/phoneticguide/rubytext/) { get; } | Ruft den Ruby-Text des Phonetikführers ab. |

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

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
