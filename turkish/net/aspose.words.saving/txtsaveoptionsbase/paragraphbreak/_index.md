---
title: TxtSaveOptionsBase.ParagraphBreak
linktitle: ParagraphBreak
articleTitle: ParagraphBreak
second_title: Aspose.Words for .NET
description: TxtSaveOptionsBase ParagraphBreak mülk. Metin formatlarında dışa aktarırken paragraf sonu olarak kullanılacak dizeyi belirtir C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/txtsaveoptionsbase/paragraphbreak/
---
## TxtSaveOptionsBase.ParagraphBreak property

Metin formatlarında dışa aktarırken paragraf sonu olarak kullanılacak dizeyi belirtir.

```csharp
public string ParagraphBreak { get; set; }
```

## Notlar

Varsayılan değer:[`CrLf`](../../../aspose.words/controlchar/crlf/).

## Örnekler

Bir .txt belgesinin özel paragraf sonuyla nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");
builder.Write("Paragraph 3.");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "TxtSaveOptions" nesnesi oluşturun
// belgeyi düz metne kaydetme şeklimizi değiştirmek için.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

Assert.AreEqual(SaveFormat.Text, txtSaveOptions.SaveFormat);

// "ParagraphBreak" değerini her paragrafın sonuna koymak istediğimiz özel bir değere ayarlayın.
txtSaveOptions.ParagraphBreak = " End of paragraph.\n\n\t";

doc.Save(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt");

Assert.AreEqual("Paragraph 1. End of paragraph.\n\n\t" +
                "Paragraph 2. End of paragraph.\n\n\t" +
                "Paragraph 3. End of paragraph.\n\n\t", docText);
```

### Ayrıca bakınız

* class [TxtSaveOptionsBase](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
