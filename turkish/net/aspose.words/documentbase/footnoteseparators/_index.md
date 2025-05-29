---
title: DocumentBase.FootnoteSeparators
linktitle: FootnoteSeparators
articleTitle: FootnoteSeparators
second_title: .NET için Aspose.Words
description: Gelişmiş biçimlendirme denetimi için DocumentBase'in FootnoteSeparators özelliğiyle belgenizdeki dipnot ve sonnot ayırıcılarına erişin ve bunları özelleştirin.
type: docs
weight: 40
url: /tr/net/aspose.words/documentbase/footnoteseparators/
---
## DocumentBase.FootnoteSeparators property

Belgede tanımlanan dipnot/sonnot ayırıcılarına erişim sağlar.

```csharp
public FootnoteSeparatorCollection FootnoteSeparators { get; }
```

## Örnekler

Dipnot ayırıcısının nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator endnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.EndnoteSeparator];
// Dipnot ayırıcısını kaldırın.
endnoteSeparator.FirstParagraph.FirstChild.Remove();
```

Dipnot ayırıcı formatının nasıl yönetileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// Dipnot ayırıcısını hizala.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### Ayrıca bakınız

* class [FootnoteSeparatorCollection](../../../aspose.words.notes/footnoteseparatorcollection/)
* class [DocumentBase](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
