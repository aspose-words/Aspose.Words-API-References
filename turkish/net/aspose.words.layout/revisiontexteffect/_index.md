---
title: Enum RevisionTextEffect
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Layout.RevisionTextEffect Sıralama. Belge metninin revizyonları için dekorasyon efektini belirtmeye olanak tanır.
type: docs
weight: 3400
url: /tr/net/aspose.words.layout/revisiontexteffect/
---
## RevisionTextEffect enumeration

Belge metninin revizyonları için dekorasyon efektini belirtmeye olanak tanır.

```csharp
public enum RevisionTextEffect
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Revize edilmiş içeriğe herhangi bir özel efekt uygulanmamıştır. Bu, şuna karşılık gelir:NoHighlight . |
| Color | `1` | Revize edilen içerik yalnızca renkli olarak vurgulanır. |
| Bold | `2` | Revize edilen içerik kalın ve renkli hale getirildi. |
| Italic | `3` | Revize edilen içerik italik ve renkli hale getirildi. |
| Underline | `4` | Revize edilen içeriğin altı çizili ve renklidir. |
| DoubleUnderline | `5` | Revize edilen içeriğin altı çift çizili ve renklidir. |
| StrikeThrough | `6` | Gözden geçirilmiş içerik konturlarla çizilmiş ve renklendirilmiştir. |
| DoubleStrikeThrough | `7` | Revize edilmiş içerik çift vuruşlu ve renklidir. |
| Hidden | `8` | Revize edilen içerik gizlendi. |

### Örnekler

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

* ad alanı [Aspose.Words.Layout](../../aspose.words.layout/)
* toplantı [Aspose.Words](../../)


