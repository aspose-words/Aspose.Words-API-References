---
title: Field.GetFieldCode
linktitle: GetFieldCode
articleTitle: GetFieldCode
second_title: .NET için Aspose.Words
description: GetFieldCode metodunu keşfedin, alan başlangıcı ve ayırıcı arasındaki metni, alt alan kodları ve sonuçları da dahil olmak üzere zahmetsizce alın. Kodlama verimliliğinizi artırın!
type: docs
weight: 110
url: /tr/net/aspose.words.fields/field/getfieldcode/
---
## GetFieldCode() {#getfieldcode}

Alan başlangıcı ile alan ayırıcısı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir.

```csharp
public string GetFieldCode()
```

## Örnekler

Alan kodu kullanılarak bir belgeye alanın nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// InsertField yönteminin bu aşırı yüklemesi eklenen alanları otomatik olarak günceller.
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

Bir alanın alan kodunun nasıl alınacağını gösterir.

```csharp
// IF alanı içinde MERGEFIELD içeren bir belgeyi aç.
Document doc = new Document(MyDir + "Nested fields.docx");
FieldIf fieldIf = (FieldIf)doc.Range.Fields[0];

// Bir alanın alan kodunu almanın iki yolu vardır:
// 1 - İç alanlarını atla:
Assert.AreEqual(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.GetFieldCode(false));

// 2 - İç alanlarını dahil et:
Assert.AreEqual($" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" ",
    fieldIf.GetFieldCode(true));

// Varsayılan olarak, GetFieldCode yöntemi iç alanları görüntüler.
Assert.AreEqual(fieldIf.GetFieldCode(), fieldIf.GetFieldCode(true));
```

### Ayrıca bakınız

* class [Field](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)

---

## GetFieldCode(*bool*) {#getfieldcode_1}

Alan başlangıcı ile alan ayırıcısı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür.

```csharp
public string GetFieldCode(bool includeChildFieldCodes)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| includeChildFieldCodes | Boolean | `doğru` eğer çocuk alan kodları dahil edilmeliyse. |

## Örnekler

Bir alanın alan kodunun nasıl alınacağını gösterir.

```csharp
// IF alanı içinde MERGEFIELD içeren bir belgeyi aç.
Document doc = new Document(MyDir + "Nested fields.docx");
FieldIf fieldIf = (FieldIf)doc.Range.Fields[0];

// Bir alanın alan kodunu almanın iki yolu vardır:
// 1 - İç alanlarını atla:
Assert.AreEqual(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.GetFieldCode(false));

// 2 - İç alanlarını dahil et:
Assert.AreEqual($" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" ",
    fieldIf.GetFieldCode(true));

// Varsayılan olarak, GetFieldCode yöntemi iç alanları görüntüler.
Assert.AreEqual(fieldIf.GetFieldCode(), fieldIf.GetFieldCode(true));
```

### Ayrıca bakınız

* class [Field](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
