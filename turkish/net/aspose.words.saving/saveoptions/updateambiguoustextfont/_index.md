---
title: SaveOptions.UpdateAmbiguousTextFont
linktitle: UpdateAmbiguousTextFont
articleTitle: UpdateAmbiguousTextFont
second_title: .NET için Aspose.Words
description: UpdateAmbiguousTextFont ile PDF'lerdeki metin netliğini artırın. Daha iyi okunabilirlik için karakter kodlarına dayalı doğru yazı tipi oluşturmayı sağlayın.
type: docs
weight: 150
url: /tr/net/aspose.words.saving/saveoptions/updateambiguoustextfont/
---
## SaveOptions.UpdateAmbiguousTextFont property

Kullanılan karakter koduna göre yazı tipi özniteliklerinin değiştirilip değiştirilmeyeceğini belirler.

```csharp
public bool UpdateAmbiguousTextFont { get; set; }
```

## Örnekler

Kullanılan karakter koduyla eşleşecek şekilde yazı tipinin nasıl güncelleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Special symbol.docx");
Run run = doc.FirstSection.Body.FirstParagraph.Runs[0];
Console.WriteLine(run.Text); // ฿
Console.WriteLine(run.Font.Name); // Arial

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.UpdateAmbiguousTextFont = true;
doc.Save(ArtifactsDir + "OoxmlSaveOptions.UpdateAmbiguousTextFont.docx", saveOptions);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.UpdateAmbiguousTextFont.docx");
run = doc.FirstSection.Body.FirstParagraph.Runs[0];
Console.WriteLine(run.Text); // ฿
Console.WriteLine(run.Font.Name); // Angsana Yeni
```

### Ayrıca bakınız

* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
