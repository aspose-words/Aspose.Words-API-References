---
title: RevisionOptions.MovedFromTextEffect
linktitle: MovedFromTextEffect
articleTitle: MovedFromTextEffect
second_title: .NET için Aspose.Words
description: DoubleStrikeThrough gibi efektlerle içerik hareket görünürlüğünü özelleştirmek için RevisionOptions' MovedFromTextEffect özelliğini keşfedin. Belgenizin netliğini artırın!
type: docs
weight: 100
url: /tr/net/aspose.words.layout/revisionoptions/movedfromtexteffect/
---
## RevisionOptions.MovedFromTextEffect property

İçeriğin taşındığı alanlara uygulanacak efekti belirtmenize olanak tanırMoving . Varsayılan değerDoubleStrikeThrough

```csharp
public RevisionTextEffect MovedFromTextEffect { get; set; }
```

## Örnekler

Revizyonların görünümünün nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Revizyonların görünümünü kontrol eden RevisionOptions nesnesini alın.
RevisionOptions revisionOptions = doc.LayoutOptions.RevisionOptions;

// Ekleme revizyonlarını yeşil ve italik olarak göster.
revisionOptions.InsertedTextColor = RevisionColor.Green;
revisionOptions.InsertedTextEffect = RevisionTextEffect.Italic;

// Silme revizyonlarını kırmızı ve kalın olarak göster.
revisionOptions.DeletedTextColor = RevisionColor.Red;
revisionOptions.DeletedTextEffect = RevisionTextEffect.Bold;

// Bir hareket revizyonunda aynı metin iki kez görünecek:
// bir kez kalkış noktasında ve bir kez varış noktasında.
// Taşınmış revizyondaki metni çift çizgiyle sarıya boya
// ve taşınan revizyonda çift altı çizili mavi.
revisionOptions.MovedFromTextColor = RevisionColor.Yellow;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.MovedToTextColor = RevisionColor.ClassicBlue;
revisionOptions.MovedToTextEffect = RevisionTextEffect.DoubleUnderline;

// Biçim revizyonlarını koyu kırmızı ve kalın olarak göster.
revisionOptions.RevisedPropertiesColor = RevisionColor.DarkRed;
revisionOptions.RevisedPropertiesEffect = RevisionTextEffect.Bold;

// Revizyonlardan etkilenen satırların yanına, sayfanın sol tarafına kalın, koyu mavi bir çubuk yerleştirin.
revisionOptions.RevisionBarsColor = RevisionColor.DarkBlue;
revisionOptions.RevisionBarsWidth = 15.0f;

// Düzeltme işaretlerini ve orijinal metni göster.
revisionOptions.ShowOriginalRevision = true;
revisionOptions.ShowRevisionMarks = true;

// Hareket, silme, biçimlendirme revizyonları ve yorumların yeşil balonlarda gösterilmesini sağlayın
// Sayfanın sağ tarafında.
revisionOptions.ShowInBalloons = ShowInBalloons.Format;
revisionOptions.CommentColor = RevisionColor.BrightGreen;

// Bu özellikler yalnızca .pdf veya .jpg gibi formatlar için geçerlidir.
doc.Save(ArtifactsDir + "Revision.RevisionOptions.pdf");
```

### Ayrıca bakınız

* enum [RevisionTextEffect](../../revisiontexteffect/)
* class [RevisionOptions](../)
* ad alanı [Aspose.Words.Layout](../../../aspose.words.layout/)
* toplantı [Aspose.Words](../../../)
