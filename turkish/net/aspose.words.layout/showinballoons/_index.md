---
title: ShowInBalloons Enum
linktitle: ShowInBalloons
articleTitle: ShowInBalloons
second_title: .NET için Aspose.Words
description: Aspose.Words.Layout.ShowInBalloons enumunun, balonlardaki görünür revizyonları kontrol ederek belge düzenlemeyi nasıl geliştirdiğini ve net işbirliğini nasıl sağladığını keşfedin.
type: docs
weight: 3860
url: /tr/net/aspose.words.layout/showinballoons/
---
## ShowInBalloons enumeration

Balonlarda hangi revizyonların işleneceğini belirtir.

```csharp
public enum ShowInBalloons
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Ekleme, silme ve biçimlendirme revizyonlarını satır içi olarak işler. |
| Format | `1` | Revizyonları satır içi olarak ekler ve siler, revizyonları balonlar halinde biçimlendirir. |
| FormatAndDelete | `2` | Revizyonları satır içi olarak ekler, balonlardaki revizyonları siler ve biçimlendirir. |

## Notlar

Düzeltmelerin balonlarda işlenmediğini unutmayınShowInAnnotations .

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

* ad alanı [Aspose.Words.Layout](../../aspose.words.layout/)
* toplantı [Aspose.Words](../../)
