---
title: Enum RevisionTextEffect
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Layout.RevisionTextEffect Sıralama. Belge metninin revizyonları için dekorasyon efekti belirlemeye izin verir.
type: docs
weight: 3200
url: /tr/net/aspose.words.layout/revisiontexteffect/
---
## RevisionTextEffect enumeration

Belge metninin revizyonları için dekorasyon efekti belirlemeye izin verir.

```csharp
public enum RevisionTextEffect
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Gözden geçirilmiş içeriğe uygulanan özel efekt yoktur. Bu şuna karşılık gelir:NoHighlight . |
| Color | `1` | Gözden geçirilmiş içerik yalnızca renkle vurgulanır. |
| Bold | `2` | Gözden geçirilmiş içerik kalın ve renkli hale getirildi. |
| Italic | `3` | Revize edilmiş içerik italik ve renkli hale getirildi. |
| Underline | `4` | Gözden geçirilmiş içeriğin altı çizili ve renkli. |
| DoubleUnderline | `5` | Revize edilmiş içeriğin altı çift çizili ve renklidir. |
| StrikeThrough | `6` | Gözden geçirilmiş içeriğin üzeri çizilir ve renklendirilir. |
| DoubleStrikeThrough | `7` | Gözden geçirilmiş içerik çift çizilir ve renklendirilir. |
| Hidden | `8` | Gözden geçirilmiş içerik gizli. |

### Örnekler

Düzeltmelerin görünümünün nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Revizyonların görünümünü kontrol eden RevisionOptions nesnesini alın.
RevisionOptions revisionOptions = doc.LayoutOptions.RevisionOptions;

// Ekleme revizyonlarını yeşil ve italik olarak işle.
revisionOptions.InsertedTextColor = RevisionColor.Green;
revisionOptions.InsertedTextEffect = RevisionTextEffect.Italic;

// Silme revizyonlarını kırmızı ve kalın olarak işle.
revisionOptions.DeletedTextColor = RevisionColor.Red;
revisionOptions.DeletedTextEffect = RevisionTextEffect.Bold;

// Aynı metin bir hareket revizyonunda iki kez görünecek:
// bir kez kalkış noktasında ve bir kez varış noktasında.
// Taşınan revizyondaki metni çift vuruşla sarıya çevir
// ve taşınan revizyonda altı çift mavi çizgili.
revisionOptions.MovedFromTextColor = RevisionColor.Yellow;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.MovedToTextColor = RevisionColor.Blue;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleUnderline;

// Format revizyonlarını koyu kırmızı ve kalın olarak işleyin.
revisionOptions.RevisedPropertiesColor = RevisionColor.DarkRed;
revisionOptions.RevisedPropertiesEffect = RevisionTextEffect.Bold;

// Sayfanın sol tarafında, revizyonlardan etkilenen satırların yanına kalın bir lacivert çubuk yerleştirin.
revisionOptions.RevisionBarsColor = RevisionColor.DarkBlue;
revisionOptions.RevisionBarsWidth = 15.0f;

// Revizyon işaretlerini ve orijinal metni göster.
revisionOptions.ShowOriginalRevision = true;
revisionOptions.ShowRevisionMarks = true;

// Yeşil balonlarda görünecek hareket, silme, biçimlendirme revizyonları ve yorumları alın
// sayfanın sağ tarafında.
revisionOptions.ShowInBalloons = ShowInBalloons.Format;
revisionOptions.CommentColor = RevisionColor.BrightGreen;

// Bu özellikler yalnızca .pdf veya .jpg gibi biçimler için geçerlidir.
doc.Save(ArtifactsDir + "Revision.RevisionOptions.pdf");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Layout](../../aspose.words.layout/)
* toplantı [Aspose.Words](../../)


