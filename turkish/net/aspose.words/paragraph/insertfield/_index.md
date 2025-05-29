---
title: Paragraph.InsertField
linktitle: InsertField
articleTitle: InsertField
second_title: .NET için Aspose.Words
description: Paragraph InsertField yöntemi ile paragraflara alanları zahmetsizce ekleyin. Belgenizin işlevselliğini artırın ve içerik yönetimini kolaylaştırın.
type: docs
weight: 290
url: /tr/net/aspose.words/paragraph/insertfield/
---
## InsertField(*[FieldType](../../../aspose.words.fields/fieldtype/), bool, [Node](../../node/), bool*) {#insertfield}

Bu paragrafa bir alan ekler.

```csharp
public Field InsertField(FieldType fieldType, bool updateField, Node refNode, bool isAfter)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fieldType | FieldType | Eklenecek alanın türü. |
| updateField | Boolean | Alanın hemen güncellenip güncellenmeyeceğini belirtir. |
| refNode | Node | Bu paragrafın içindeki referans düğümü (eğer*refNode* dır`hükümsüz`, daha sonra paragrafın sonuna eklenir). |
| isAfter | Boolean | Alanın referans düğümünden önce mi sonra mı ekleneceğini belirtir. |

### Geri dönüş değeri

A[`Field`](../../../aspose.words.fields/field/) eklenen alanı temsil eden nesne.

## Örnekler

Bir paragrafa alan eklemenin çeşitli yollarını gösterir.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Aşağıda bir paragrafa alan eklemenin üç yolu bulunmaktadır.
// 1 - Bir paragrafın alt düğümlerinden birinin ardından paragrafa bir YAZAR alanı ekle:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Paragrafın alt düğümlerinden birinin ardından bir QUOTE alanı ekle:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Paragrafın alt düğümlerinden birinin önüne bir QUOTE alanı ekle,
// ve bir yer tutucu değerin görüntülenmesini sağlayın:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Bu alan, biz güncelleyene kadar yer tutucu değerini görüntüleyecektir.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Ayrıca bakınız

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [Node](../../node/)
* class [Paragraph](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## InsertField(*string, [Node](../../node/), bool*) {#insertfield_1}

Bu paragrafa bir alan ekler.

```csharp
public Field InsertField(string fieldCode, Node refNode, bool isAfter)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fieldCode | String | Eklenecek alan kodu (süslü parantez olmadan). |
| refNode | Node | Bu paragrafın içindeki referans düğümü (eğer*refNode* dır`hükümsüz`, daha sonra paragrafın sonuna eklenir). |
| isAfter | Boolean | Alanın referans düğümünden önce mi sonra mı ekleneceğini belirtir. |

### Geri dönüş değeri

A[`Field`](../../../aspose.words.fields/field/) eklenen alanı temsil eden nesne.

## Örnekler

Bir paragrafa alan eklemenin çeşitli yollarını gösterir.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Aşağıda bir paragrafa alan eklemenin üç yolu bulunmaktadır.
// 1 - Bir paragrafın alt düğümlerinden birinin ardından paragrafa bir YAZAR alanı ekle:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Paragrafın alt düğümlerinden birinin ardından bir QUOTE alanı ekle:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Paragrafın alt düğümlerinden birinin önüne bir QUOTE alanı ekle,
// ve bir yer tutucu değerin görüntülenmesini sağlayın:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Bu alan, biz güncelleyene kadar yer tutucu değerini görüntüleyecektir.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Ayrıca bakınız

* class [Field](../../../aspose.words.fields/field/)
* class [Node](../../node/)
* class [Paragraph](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## InsertField(*string, string, [Node](../../node/), bool*) {#insertfield_2}

Bu paragrafa bir alan ekler.

```csharp
public Field InsertField(string fieldCode, string fieldValue, Node refNode, bool isAfter)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fieldCode | String | Eklenecek alan kodu (süslü parantez olmadan). |
| fieldValue | String | Eklenecek alan değeri. Geç`hükümsüz` değeri olmayan alanlar için. |
| refNode | Node | Bu paragrafın içindeki referans düğümü (eğer*refNode* dır`hükümsüz`, daha sonra paragrafın sonuna eklenir). |
| isAfter | Boolean | Alanın referans düğümünden önce mi sonra mı ekleneceğini belirtir. |

### Geri dönüş değeri

A[`Field`](../../../aspose.words.fields/field/) eklenen alanı temsil eden nesne.

## Örnekler

Bir paragrafa alan eklemenin çeşitli yollarını gösterir.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Aşağıda bir paragrafa alan eklemenin üç yolu bulunmaktadır.
// 1 - Bir paragrafın alt düğümlerinden birinin ardından paragrafa bir YAZAR alanı ekle:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Paragrafın alt düğümlerinden birinin ardından bir QUOTE alanı ekle:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Paragrafın alt düğümlerinden birinin önüne bir QUOTE alanı ekle,
// ve bir yer tutucu değerin görüntülenmesini sağlayın:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Bu alan, biz güncelleyene kadar yer tutucu değerini görüntüleyecektir.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Ayrıca bakınız

* class [Field](../../../aspose.words.fields/field/)
* class [Node](../../node/)
* class [Paragraph](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
