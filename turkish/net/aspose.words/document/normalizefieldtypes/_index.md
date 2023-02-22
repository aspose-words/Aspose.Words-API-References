---
title: Document.NormalizeFieldTypes
second_title: Aspose.Words for .NET API Referansı
description: Document yöntem. Alan türü değerlerini değiştirirFieldType nınninFieldStart FieldSeparator FieldEnd alan kodlarında yer alan alan türlerine karşılık gelecek şekilde belgenin tamamında.
type: docs
weight: 610
url: /tr/net/aspose.words/document/normalizefieldtypes/
---
## Document.NormalizeFieldTypes method

Alan türü değerlerini değiştirir[`FieldType`](../../../aspose.words.fields/fieldchar/fieldtype/) nın-nin[`FieldStart`](../../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../../aspose.words.fields/fieldend/) alan kodlarında yer alan alan türlerine karşılık gelecek şekilde belgenin tamamında.

```csharp
public void NormalizeFieldTypes()
```

### Notlar

Alan türlerini etkileyen belge değişikliklerinden sonra bu yöntemi kullanın.

Belgenin belirli bir bölümündeki alan türü değerlerini değiştirmek için[`NormalizeFieldTypes`](../../range/normalizefieldtypes/).

### Örnekler

Bir alanın türünün alan koduyla nasıl güncel tutulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE", null);

// Aspose.Words alan tiplerini alan kodlarına göre otomatik olarak algılar.
Assert.AreEqual(FieldType.FieldDate, field.Type);

// Alan kodunu belirleyen alanın ham metnini manuel olarak değiştirin.
Run fieldText = (Run)doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Run, true)[0];

// Alan kodunun değiştirilmesi, bu alanın farklı bir türe dönüşmesine neden oldu,
// ancak alanın tür özellikleri hala eski türü gösteriyor.
Assert.AreEqual("PAGE", field.GetFieldCode());
Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual(FieldType.FieldDate, field.Start.FieldType);
Assert.AreEqual(FieldType.FieldDate, field.Separator.FieldType);
Assert.AreEqual(FieldType.FieldDate, field.End.FieldType);

// Geçerli değeri görüntülemek için bu özellikleri bu yöntemle güncelleyin.
doc.NormalizeFieldTypes();

Assert.AreEqual(FieldType.FieldPage, field.Type);
Assert.AreEqual(FieldType.FieldPage, field.Start.FieldType);
Assert.AreEqual(FieldType.FieldPage, field.Separator.FieldType); 
Assert.AreEqual(FieldType.FieldPage, field.End.FieldType);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)


