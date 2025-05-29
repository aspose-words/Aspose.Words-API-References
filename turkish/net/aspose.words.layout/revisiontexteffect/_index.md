---
title: RevisionTextEffect Enum
linktitle: RevisionTextEffect
articleTitle: RevisionTextEffect
second_title: .NET için Aspose.Words
description: Benzersiz metin dekorasyon efektleriyle belge revizyonlarını geliştirmek için Aspose.Words.Layout.RevisionTextEffect enum'unu keşfedin. Düzenleme deneyiminizi yükseltin!
type: docs
weight: 3850
url: /tr/net/aspose.words.layout/revisiontexteffect/
---
## RevisionTextEffect enumeration

Belge metninin revizyonları için dekorasyon efektini belirtmeye izin verir.

```csharp
public enum RevisionTextEffect
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Gözden geçirilmiş içerikte özel efekt uygulanmamıştır. Bu, şuna karşılık gelir:NoHighlight . |
| Color | `1` | Gözden geçirilmiş içerik yalnızca renkle vurgulanır. |
| Bold | `2` | Gözden geçirilen içerik kalınlaştırıldı ve renklendirildi. |
| Italic | `3` | Gözden geçirilen içerik italik hale getirildi ve renklendirildi. |
| Underline | `4` | Gözden geçirilmiş içerik altı çizili ve renklidir. |
| DoubleUnderline | `5` | Gözden geçirilmiş içerik çift altı çizili ve renklidir. |
| StrikeThrough | `6` | Gözden geçirilmiş içerik çizilmiş ve renklendirilmiştir. |
| DoubleStrikeThrough | `7` | Gözden geçirilmiş içerik çift çizilmiş ve renklendirilmiştir. |
| Hidden | `8` | Gözden geçirilmiş içerik gizlidir. |

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
