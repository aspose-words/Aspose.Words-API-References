---
title: Enum HeightRule
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.HeightRule Sıralama. Bir nesnenin yüksekliğini belirleme kuralını belirtir.
type: docs
weight: 3130
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
| AtLeast | `0` | Yükseklik en az nokta cinsinden belirtilen yükseklik olacaktır. Gerekirse, bir nesnenin içindeki tüm metni barındıracak şekilde büyüyecektir. |
| Exactly | `1` | Yükseklik tam olarak nokta cinsinden belirtilir. Lütfen metnin bu yükseklikteki nesnenin içine sığamaması durumunda kesik görüneceğini unutmayın. |
| Auto | `2` | Yükseklik, bir nesnenin içindeki tüm metni barındıracak şekilde otomatik olarak artacaktır. |

### Örnekler

Satırların bir belge oluşturucuyla nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// İkinci bir satır başlatın ve ardından yüksekliğini yapılandırın. Oluşturucu bu ayarları aşağıdakilere uygulayacaktır:
// geçerli satırın yanı sıra daha sonra oluşturacağı yeni satırlar.
builder.EndRow();

RowFormat rowFormat = builder.RowFormat;
rowFormat.Height = 100;
rowFormat.HeightRule = HeightRule.Exactly;

builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.EndTable();

// İlk satır dolgunun yeniden yapılandırılmasından etkilenmedi ve hala varsayılan değerleri koruyor.
Assert.AreEqual(0.0d, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);

Assert.AreEqual(100.0d, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


