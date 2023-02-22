---
title: Enum ShowInBalloons
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Layout.ShowInBalloons Sıralama. Balonlarda hangi revizyonların oluşturulacağını belirtir.
type: docs
weight: 3210
url: /tr/net/aspose.words.layout/showinballoons/
---
## ShowInBalloons enumeration

Balonlarda hangi revizyonların oluşturulacağını belirtir.

```csharp
public enum ShowInBalloons
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Revizyonları satır içinde ekler, siler ve biçimlendirir. |
| Format | `1` | Revizyonları satır içinde ekler ve siler, revizyonları balonlarda biçimlendirir. |
| FormatAndDelete | `2` | İşler, revizyonları satır içinde ekler, revizyonları balonlarda siler ve biçimlendirir. |

### Notlar

için revizyonların balonlarda gösterilmediğini unutmayın.ShowInAnnotations .

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


