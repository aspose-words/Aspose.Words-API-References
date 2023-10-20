---
title: RevisionOptions.RevisedPropertiesColor
linktitle: RevisedPropertiesColor
articleTitle: RevisedPropertiesColor
second_title: Aspose.Words for .NET
description: RevisionOptions RevisedPropertiesColor mülk. Biçimlendirme özelliklerinde değişiklik yapılarak içerik için kullanılacak rengi belirtmeye olanak tanırFormatChange Varsayılan değerNoHighlight  C#'da.
type: docs
weight: 110
url: /tr/net/aspose.words.layout/revisionoptions/revisedpropertiescolor/
---
## RevisionOptions.RevisedPropertiesColor property

Biçimlendirme özelliklerinde değişiklik yapılarak içerik için kullanılacak rengi belirtmeye olanak tanırFormatChange Varsayılan değer:NoHighlight .

```csharp
public RevisionColor RevisedPropertiesColor { get; set; }
```

## Örnekler

Revizyonların görünümünün nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Revizyonların görünümünü kontrol eden RevisionOptions nesnesini alın.
RevisionOptions revisionOptions = doc.LayoutOptions.RevisionOptions;

// Ekleme revizyonlarını yeşil ve italik olarak işle.
revisionOptions.InsertedTextColor = RevisionColor.Green;
revisionOptions.InsertedTextEffect = RevisionTextEffect.Italic;

// Silme düzeltmelerini kırmızı ve kalın harflerle işleyin.
revisionOptions.DeletedTextColor = RevisionColor.Red;
revisionOptions.DeletedTextEffect = RevisionTextEffect.Bold;

// Aynı metin bir hareket revizyonunda iki kez görünecektir:
// bir kez kalkış noktasında ve bir kez varış noktasında.
// Taşınan revizyondaki metni çift çizgiyle sarıya dönüştür
// ve taşınan revizyonda çift altı çizili mavi.
revisionOptions.MovedFromTextColor = RevisionColor.Yellow;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.MovedToTextColor = RevisionColor.ClassicBlue;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleUnderline;

// Format revizyonlarını koyu kırmızı ve kalın olarak işleyin.
revisionOptions.RevisedPropertiesColor = RevisionColor.DarkRed;
revisionOptions.RevisedPropertiesEffect = RevisionTextEffect.Bold;

// Sayfanın sol tarafına, revizyonlardan etkilenen satırların yanına kalın, lacivert bir çubuk yerleştirin.
revisionOptions.RevisionBarsColor = RevisionColor.DarkBlue;
revisionOptions.RevisionBarsWidth = 15.0f;

// Revizyon işaretlerini ve orijinal metni göster.
revisionOptions.ShowOriginalRevision = true;
revisionOptions.ShowRevisionMarks = true;

// Hareket, silme, biçimlendirme revizyonları ve yorumların yeşil balonlarla gösterilmesini sağlayın
//sayfanın sağ tarafında.
revisionOptions.ShowInBalloons = ShowInBalloons.Format;
revisionOptions.CommentColor = RevisionColor.BrightGreen;

// Bu özellikler yalnızca .pdf veya .jpg gibi formatlar için geçerlidir.
doc.Save(ArtifactsDir + "Revision.RevisionOptions.pdf");
```

### Ayrıca bakınız

* enum [RevisionColor](../../revisioncolor/)
* class [RevisionOptions](../)
* ad alanı [Aspose.Words.Layout](../../../aspose.words.layout/)
* toplantı [Aspose.Words](../../../)
