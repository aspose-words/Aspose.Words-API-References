---
title: Document.NormalizeFieldTypes
linktitle: NormalizeFieldTypes
articleTitle: NormalizeFieldTypes
second_title: .NET için Aspose.Words
description: NormalizeFieldTypes yöntemiyle belgenizi optimize edin ve gelişmiş tutarlılık ve doğruluk için tüm alan türü değerlerinin alan kodlarıyla hizalanmasını sağlayın.
type: docs
weight: 670
url: /tr/net/aspose.words/document/normalizefieldtypes/
---
## Document.NormalizeFieldTypes method

Alan türü değerlerini değiştirir[`FieldType`](../../../aspose.words.fields/fieldchar/fieldtype/) ile ilgili[`FieldStart`](../../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../../aspose.words.fields/fieldend/) tüm belgede, alan kodlarında bulunan alan türlerine karşılık gelecek şekilde.

```csharp
public void NormalizeFieldTypes()
```

## Notlar

Alan türlerini etkileyen belge değişikliklerinden sonra bu yöntemi kullanın.

Belgenin belirli bir bölümündeki alan türü değerlerini değiştirmek için şunu kullanın:[`NormalizeFieldTypes`](../../range/normalizefieldtypes/).

## Örnekler

Bir alanın türünün alan koduyla güncel tutulmasının nasıl sağlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE", null);

// Aspose.Words alan kodlarına göre alan türlerini otomatik olarak algılar.
Assert.AreEqual(FieldType.FieldDate, field.Type);

// Alan kodunu belirleyen alanın ham metnini manuel olarak değiştirin.
Run fieldText = (Run)doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Run, true)[0];
fieldText.Text = "PAGE";

// Alan kodunun değiştirilmesi bu alanı farklı bir türe dönüştürdü,
// ancak alanın tür özellikleri hala eski türü gösteriyor.
Assert.AreEqual("PAGE", field.GetFieldCode());
Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual(FieldType.FieldDate, field.Start.FieldType);
Assert.AreEqual(FieldType.FieldDate, field.Separator.FieldType);
Assert.AreEqual(FieldType.FieldDate, field.End.FieldType);

// Bu metodu kullanarak o özellikleri güncelleyip geçerli değeri görüntüleyebilirsiniz.
doc.NormalizeFieldTypes();

Assert.AreEqual(FieldType.FieldPage, field.Type);
Assert.AreEqual(FieldType.FieldPage, field.Start.FieldType);
Assert.AreEqual(FieldType.FieldPage, field.Separator.FieldType);
Assert.AreEqual(FieldType.FieldPage, field.End.FieldType);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
