---
title: Paragraph.InsertField
linktitle: InsertField
articleTitle: InsertField
second_title: Aspose.Words for .NET
description: Paragraph InsertField yöntem. Bu paragrafa bir alan ekler C#'da.
type: docs
weight: 270
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
| refNode | Node | Bu paragrafın içindeki referans düğümü (eğer*refNode* dır-dir`hükümsüz`, daha sonra paragrafın sonuna eklenir). |
| isAfter | Boolean | Alanın referans düğümünden sonra mı yoksa önce mi ekleneceği. |

### Geri dönüş değeri

A[`Field`](../../../aspose.words.fields/field/) eklenen alanı temsil eden nesne.

## Örnekler

Bir paragrafa alan eklemenin çeşitli yollarını gösterir.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Aşağıda paragrafa alan eklemenin üç yolu verilmiştir.
// 1 - Paragrafın alt düğümlerinden birinden sonra paragrafa bir AUTHOR alanı ekleyin:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Paragrafın alt düğümlerinden birinden sonra bir QUOTE alanı ekleyin:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Paragrafın alt düğümlerinden birinin önüne bir QUOTE alanı ekleyin,
// ve bir yer tutucu değeri göstermesini sağlayın:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Bu alan, biz güncelleyene kadar yer tutucu değerini gösterecektir.
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
| fieldCode | String | Eklenecek alan kodu (küme parantezleri olmadan). |
| refNode | Node | Bu paragrafın içindeki referans düğümü (eğer*refNode* dır-dir`hükümsüz`, daha sonra paragrafın sonuna eklenir). |
| isAfter | Boolean | Alanın referans düğümünden sonra mı yoksa önce mi ekleneceği. |

### Geri dönüş değeri

A[`Field`](../../../aspose.words.fields/field/) eklenen alanı temsil eden nesne.

## Örnekler

Bir paragrafa alan eklemenin çeşitli yollarını gösterir.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Aşağıda paragrafa alan eklemenin üç yolu verilmiştir.
// 1 - Paragrafın alt düğümlerinden birinden sonra paragrafa bir AUTHOR alanı ekleyin:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Paragrafın alt düğümlerinden birinden sonra bir QUOTE alanı ekleyin:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Paragrafın alt düğümlerinden birinin önüne bir QUOTE alanı ekleyin,
// ve bir yer tutucu değeri göstermesini sağlayın:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Bu alan, biz güncelleyene kadar yer tutucu değerini gösterecektir.
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
| fieldCode | String | Eklenecek alan kodu (küme parantezleri olmadan). |
| fieldValue | String | Eklenecek alan değeri. Geçmek`hükümsüz` değeri olmayan alanlar için. |
| refNode | Node | Bu paragrafın içindeki referans düğümü (eğer*refNode* dır-dir`hükümsüz`, daha sonra paragrafın sonuna eklenir). |
| isAfter | Boolean | Alanın referans düğümünden sonra mı yoksa önce mi ekleneceği. |

### Geri dönüş değeri

A[`Field`](../../../aspose.words.fields/field/) eklenen alanı temsil eden nesne.

## Örnekler

Bir paragrafa alan eklemenin çeşitli yollarını gösterir.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Aşağıda paragrafa alan eklemenin üç yolu verilmiştir.
// 1 - Paragrafın alt düğümlerinden birinden sonra paragrafa bir AUTHOR alanı ekleyin:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Paragrafın alt düğümlerinden birinden sonra bir QUOTE alanı ekleyin:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Paragrafın alt düğümlerinden birinin önüne bir QUOTE alanı ekleyin,
// ve bir yer tutucu değeri göstermesini sağlayın:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Bu alan, biz güncelleyene kadar yer tutucu değerini gösterecektir.
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
