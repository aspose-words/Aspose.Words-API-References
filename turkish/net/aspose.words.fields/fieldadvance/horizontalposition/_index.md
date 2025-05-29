---
title: FieldAdvance.HorizontalPosition
linktitle: HorizontalPosition
articleTitle: HorizontalPosition
second_title: .NET için Aspose.Words
description: FieldAdvance Yatay Pozisyon özelliğini keşfedin, belgelerinizde hassas düzen kontrolü için metin konumlandırmasını kolayca ayarlayın. Biçimlendirmenizi bugün geliştirin!
type: docs
weight: 30
url: /tr/net/aspose.words.fields/fieldadvance/horizontalposition/
---
## FieldAdvance.HorizontalPosition property

Alanı takip eden metnin yatay olarak sütun, çerçeve veya metin kutusunun sol kenarından hareket ettirileceği nokta sayısını alır veya ayarlar.

```csharp
public string HorizontalPosition { get; set; }
```

## Örnekler

ADVANCE alanının nasıl ekleneceğini ve özelliklerinin nasıl düzenleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This text is in its normal place.");

// Aşağıda, ADVANCE alanını takip eden metnin konumunu ayarlamak için iki yol gösterilmektedir.
// ADVANCE alanının etkileri paragraf bitene kadar uygulanmaya devam eder,
// veya başka bir ADVANCE alanı ofset/koordinat değerlerini günceller.
// 1 - Yönsel bir ofset belirtin:
FieldAdvance field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.RightOffset = "5";
field.UpOffset = "5";

Assert.AreEqual(" ADVANCE  \\r 5 \\u 5", field.GetFieldCode());

builder.Write("This text will be moved up and to the right.");

field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.DownOffset = "5";
field.LeftOffset = "100";

Assert.AreEqual(" ADVANCE  \\d 5 \\l 100", field.GetFieldCode());

builder.Writeln("This text is moved down and to the left, overlapping the previous text.");

// 2 - Metni koordinatlarla belirtilen bir konuma taşı:
field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.HorizontalPosition = "-100";
field.VerticalPosition = "200";

Assert.AreEqual(" ADVANCE  \\x -100 \\y 200", field.GetFieldCode());

builder.Write("This text is in a custom position.");

doc.Save(ArtifactsDir + "Field.ADVANCE.docx");
```

### Ayrıca bakınız

* class [FieldAdvance](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
