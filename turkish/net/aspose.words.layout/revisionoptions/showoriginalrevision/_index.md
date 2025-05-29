---
title: RevisionOptions.ShowOriginalRevision
linktitle: ShowOriginalRevision
articleTitle: ShowOriginalRevision
second_title: .NET için Aspose.Words
description: Belge revizyonlarınızı ShowOriginalRevision özelliğiyle kontrol edin. Daha net içgörüler için orijinal ve revize edilmiş metin arasında kolayca geçiş yapın. Varsayılan, false.
type: docs
weight: 190
url: /tr/net/aspose.words.layout/revisionoptions/showoriginalrevision/
---
## RevisionOptions.ShowOriginalRevision property

Orijinal metnin düzeltilmiş metin yerine gösterilip gösterilmeyeceğini belirtmeye olanak tanır. Varsayılan değer`YANLIŞ` .

```csharp
public bool ShowOriginalRevision { get; set; }
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

* class [RevisionOptions](../)
* ad alanı [Aspose.Words.Layout](../../../aspose.words.layout/)
* toplantı [Aspose.Words](../../../)
