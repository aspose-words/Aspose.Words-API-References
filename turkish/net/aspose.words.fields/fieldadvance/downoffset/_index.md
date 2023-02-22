---
title: FieldAdvance.DownOffset
second_title: Aspose.Words for .NET API Referansı
description: FieldAdvance mülk. Alanı takip eden metnin aşağı taşınması gereken nokta sayısını alır veya ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldadvance/downoffset/
---
## FieldAdvance.DownOffset property

Alanı takip eden metnin aşağı taşınması gereken nokta sayısını alır veya ayarlar.

```csharp
public string DownOffset { get; set; }
```

### Örnekler

GELİŞMİŞ alanının nasıl ekleneceğini ve özelliklerinin nasıl düzenleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This text is in its normal place.");

// Aşağıda, onu takip eden metnin konumunu ayarlamak için GELİŞMİŞ alanını kullanmanın iki yolu bulunmaktadır.
// ADVANCE alanının etkileri paragraf bitene kadar uygulanmaya devam eder,
// veya başka bir GELİŞME alanı, ofset/koordinat değerlerini günceller.
// 1 - Bir yön ofseti belirtin:
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

// 2 - Metni koordinatlarla belirtilen bir konuma taşıyın:
field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.HorizontalPosition = "-100";
field.VerticalPosition = "200";

Assert.AreEqual(" ADVANCE  \\x -100 \\y 200", field.GetFieldCode());

builder.Write("This text is in a custom position.");

doc.Save(ArtifactsDir + "Field.ADVANCE.docx");
```

### Ayrıca bakınız

* class [FieldAdvance](../)
* ad alanı [Aspose.Words.Fields](../../fieldadvance/)
* toplantı [Aspose.Words](../../../)


