---
title: InsertField
second_title: Aspose.Words for .NET API Referansı
description: Bu paragrafa bir alan ekler.
type: docs
weight: 270
url: /tr/net/aspose.words/paragraph/insertfield/
---
## InsertField(FieldType, bool, Node, bool) {#insertfield}

Bu paragrafa bir alan ekler.

```csharp
public Field InsertField(FieldType fieldType, bool updateField, Node refNode, bool isAfter)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fieldType | FieldType | Eklenecek alanın türü. |
| updateField | Boolean | Alanın hemen güncellenip güncellenmeyeceğini belirtir. |
| refNode | Node | Bu paragrafın içindeki referans düğümü (refNode boşsa, paragrafın sonuna eklenir). |
| isAfter | Boolean | Alanın referans düğümden sonra mı önce mi ekleneceği. |

### Geri dönüş değeri

A[`Field`](../../../aspose.words.fields/field) eklenen alanı temsil eden nesne.

### Örnekler

Paragrafa alan eklemenin çeşitli yollarını gösterir.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Aşağıda bir paragrafa alan eklemenin üç yolu vardır.
// 1 - Paragrafın alt düğümlerinden birinden sonra bir paragrafa YAZAR alanı ekleyin:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Paragrafın alt düğümlerinden birinin arkasına bir QUOTE alanı ekleyin:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Paragrafın alt düğümlerinden birinin önüne bir QUOTE alanı ekleyin,
// ve bir yer tutucu değeri göstermesini sağlayın:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Bu alan, biz güncellenene kadar yer tutucu değerini gösterecektir.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Ayrıca bakınız

* class [Field](../../../aspose.words.fields/field)
* enum [FieldType](../../../aspose.words.fields/fieldtype)
* class [Node](../../node)
* class [Paragraph](../../paragraph)
* ad alanı [Aspose.Words](../../paragraph)
* toplantı [Aspose.Words](../../../)

---

## InsertField(string, Node, bool) {#insertfield_1}

Bu paragrafa bir alan ekler.

```csharp
public Field InsertField(string fieldCode, Node refNode, bool isAfter)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fieldCode | String | Eklenecek alan kodu (kıvrımlı parantezler olmadan). |
| refNode | Node | Bu paragrafın içindeki referans düğümü (refNode boşsa, paragrafın sonuna eklenir). |
| isAfter | Boolean | Alanın referans düğümden sonra mı önce mi ekleneceği. |

### Geri dönüş değeri

A[`Field`](../../../aspose.words.fields/field) eklenen alanı temsil eden nesne.

### Örnekler

Paragrafa alan eklemenin çeşitli yollarını gösterir.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Aşağıda bir paragrafa alan eklemenin üç yolu vardır.
// 1 - Paragrafın alt düğümlerinden birinden sonra bir paragrafa YAZAR alanı ekleyin:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Paragrafın alt düğümlerinden birinin arkasına bir QUOTE alanı ekleyin:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Paragrafın alt düğümlerinden birinin önüne bir QUOTE alanı ekleyin,
// ve bir yer tutucu değeri göstermesini sağlayın:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Bu alan, biz güncellenene kadar yer tutucu değerini gösterecektir.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Ayrıca bakınız

* class [Field](../../../aspose.words.fields/field)
* class [Node](../../node)
* class [Paragraph](../../paragraph)
* ad alanı [Aspose.Words](../../paragraph)
* toplantı [Aspose.Words](../../../)

---

## InsertField(string, string, Node, bool) {#insertfield_2}

Bu paragrafa bir alan ekler.

```csharp
public Field InsertField(string fieldCode, string fieldValue, Node refNode, bool isAfter)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fieldCode | String | Eklenecek alan kodu (kıvrımlı parantezler olmadan). |
| fieldValue | String | Eklenecek alan değeri. Değeri olmayan alanlar için null iletin. |
| refNode | Node | Bu paragrafın içindeki referans düğümü (refNode boşsa, paragrafın sonuna eklenir). |
| isAfter | Boolean | Alanın referans düğümden sonra mı önce mi ekleneceği. |

### Geri dönüş değeri

A[`Field`](../../../aspose.words.fields/field) eklenen alanı temsil eden nesne.

### Örnekler

Paragrafa alan eklemenin çeşitli yollarını gösterir.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Aşağıda bir paragrafa alan eklemenin üç yolu vardır.
// 1 - Paragrafın alt düğümlerinden birinden sonra bir paragrafa YAZAR alanı ekleyin:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Paragrafın alt düğümlerinden birinin arkasına bir QUOTE alanı ekleyin:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Paragrafın alt düğümlerinden birinin önüne bir QUOTE alanı ekleyin,
// ve bir yer tutucu değeri göstermesini sağlayın:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Bu alan, biz güncellenene kadar yer tutucu değerini gösterecektir.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Ayrıca bakınız

* class [Field](../../../aspose.words.fields/field)
* class [Node](../../node)
* class [Paragraph](../../paragraph)
* ad alanı [Aspose.Words](../../paragraph)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
