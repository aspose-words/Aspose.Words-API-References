---
title: ListLevel.CustomNumberStyleFormat
linktitle: CustomNumberStyleFormat
articleTitle: CustomNumberStyleFormat
second_title: Aspose.Words für .NET
description: Passen Sie Ihre Listenebenen mit der ListLevel CustomNumberStyleFormat-Eigenschaft an. Legen Sie einfach eindeutige Zahlenformate für eine verbesserte Dokumentgestaltung fest.
type: docs
weight: 20
url: /de/net/aspose.words.lists/listlevel/customnumberstyleformat/
---
## ListLevel.CustomNumberStyleFormat property

Ruft das benutzerdefinierte Zahlenformat für diese Listenebene ab oder legt es fest. Beispiel: "a, ç, ĝ, ...".

```csharp
public string CustomNumberStyleFormat { get; set; }
```

## Beispiele

Zeigt, wie das Kundennummernformat festgelegt wird.

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

doc.UpdateListLabels();

ParagraphCollection paras = doc.FirstSection.Body.Paragraphs;
Assert.AreEqual("001.", paras[0].ListLabel.LabelString);
Assert.AreEqual("0001.", paras[1].ListLabel.LabelString);
Assert.AreEqual("0002.", paras[2].ListLabel.LabelString);

paras[1].ListFormat.ListLevel.CustomNumberStyleFormat = "001, 002, 003, ...";

doc.UpdateListLabels();

Assert.AreEqual("001.", paras[0].ListLabel.LabelString);
Assert.AreEqual("001.", paras[1].ListLabel.LabelString);
Assert.AreEqual("002.", paras[2].ListLabel.LabelString);
```

Zeigt, wie Sie das Format für eine Liste mit dem benutzerdefinierten Zahlenstil erhalten.

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

ListLevel listLevel = doc.FirstSection.Body.Paragraphs[0].ListFormat.ListLevel;

string customNumberStyleFormat = string.Empty;

if (listLevel.NumberStyle == NumberStyle.Custom)
    customNumberStyleFormat = listLevel.CustomNumberStyleFormat;

Assert.AreEqual("001, 002, 003, ...", customNumberStyleFormat);

// Wir können den Wert für den angegebenen Index des Listenelements abrufen.
Assert.AreEqual("iv", ListLevel.GetEffectiveValue(4, NumberStyle.LowercaseRoman, null));
Assert.AreEqual("005", ListLevel.GetEffectiveValue(5, NumberStyle.Custom, customNumberStyleFormat));
```

### Siehe auch

* class [ListLevel](../)
* namensraum [Aspose.Words.Lists](../../../aspose.words.lists/)
* Montage [Aspose.Words](../../../)
