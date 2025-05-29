---
title: HeightRule Enum
linktitle: HeightRule
articleTitle: HeightRule
second_title: .NET için Aspose.Words
description: Belgelerdeki nesne yüksekliği üzerinde hassas kontrol için Aspose.Words.HeightRule enum'unu keşfedin. Bu temel özellik ile iş akışınızı optimize edin!
type: docs
weight: 3560
url: /tr/net/aspose.words/heightrule/
---
## HeightRule enumeration

Bir nesnenin yüksekliğini belirleme kuralını belirtir.

```csharp
public enum HeightRule
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| AtLeast | `0` | Yükseklik en azından belirtilen yükseklik kadar olacaktır. Gerekirse, nesnenin içindeki tüm metni barındırmak için büyüyecektir. |
| Exactly | `1` | Yükseklik tam olarak noktalarla belirtilir. Lütfen metnin bu yükseklikteki nesnenin içine sığmaması durumunda kesilmiş görüneceğini unutmayın. |
| Auto | `2` | Yükseklik, nesnenin içindeki tüm metni barındıracak şekilde otomatik olarak artacaktır. |

## Örnekler

Belge oluşturucuyla satırların nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// İkinci bir satır başlatın ve ardından yüksekliğini yapılandırın. Oluşturucu bu ayarları uygulayacaktır
// mevcut satırı ve sonrasında oluşturduğu yeni satırlar.
builder.EndRow();

RowFormat rowFormat = builder.RowFormat;
rowFormat.Height = 100;
rowFormat.HeightRule = HeightRule.Exactly;

builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.EndTable();

// İlk satır, dolgu yeniden yapılandırmasından etkilenmedi ve hala varsayılan değerleri koruyor.
Assert.AreEqual(0.0d, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);

Assert.AreEqual(100.0d, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
