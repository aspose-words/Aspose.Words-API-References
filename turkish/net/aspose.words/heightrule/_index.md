---
title: HeightRule
second_title: Aspose.Words for .NET API Referansı
description: Bir nesnenin yüksekliğini belirleme kuralını belirtir.
type: docs
weight: 2950
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
| AtLeast | `0` | Yükseklik, en az puan olarak belirtilen yükseklik olacaktır. Gerekirse, bir nesnenin içindeki tüm metni barındırmak için büyüyecektir. |
| Exactly | `1` | Yükseklik tam olarak nokta olarak belirtilir. Lütfen metnin bu yükseklikteki nesnenin içine sığmaması ise, kesilmiş olarak görüneceğini unutmayın. |
| Auto | `2` | Bir nesnenin içindeki tüm metni barındırmak için yükseklik otomatik olarak büyür. |

### Örnekler

Belge oluşturucu ile satırların nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// İkinci bir satır başlatın ve ardından yüksekliğini yapılandırın. Oluşturucu bu ayarları
// mevcut satırı ve daha sonra oluşturduğu yeni satırlar.
builder.EndRow();

RowFormat rowFormat = builder.RowFormat;
rowFormat.Height = 100;
rowFormat.HeightRule = HeightRule.Exactly;

builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.EndTable();

// İlk satır, dolgu yeniden yapılandırmasından etkilenmedi ve hala varsayılan değerleri tutuyor.
Assert.AreEqual(0.0d, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);

Assert.AreEqual(100.0d, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
