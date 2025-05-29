---
title: RevisionOptions.ShowInBalloons
linktitle: ShowInBalloons
articleTitle: ShowInBalloons
second_title: .NET için Aspose.Words
description: RevisionOptions ShowInBalloons özelliğini keşfedin! Gelişmiş belge netliği için balonlardaki revizyon görünürlüğünü kontrol edin. Varsayılan Hiçbiri'dir.
type: docs
weight: 180
url: /tr/net/aspose.words.layout/revisionoptions/showinballoons/
---
## RevisionOptions.ShowInBalloons property

Revizyonların balonlarda işlenip işlenmeyeceğini belirtmeye izin verir. Varsayılan değerNone .

```csharp
public ShowInBalloons ShowInBalloons { get; set; }
```

## Notlar

Düzeltmelerin balonlarda işlenmediğini unutmayınShowInAnnotations .

## Örnekler

Revizyonların balonlarda nasıl görüntüleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Varsayılan olarak, revizyon olan metin, revizyon olmayan diğer metinden ayırt edilebilmesi için farklı bir renge sahiptir.
// Sayfanın sağ kenar boşluğunda bir balon içinde her revizyon hakkında daha fazla ayrıntı göstermek için bir revizyon seçeneği ayarlayın.
doc.LayoutOptions.RevisionOptions.ShowInBalloons = ShowInBalloons.FormatAndDelete;
doc.Save(ArtifactsDir + "Revision.ShowRevisionBalloons.pdf");
```

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

* enum [ShowInBalloons](../../showinballoons/)
* class [RevisionOptions](../)
* ad alanı [Aspose.Words.Layout](../../../aspose.words.layout/)
* toplantı [Aspose.Words](../../../)
