---
title: Paragraph.AppendField
second_title: Aspose.Words for .NET API Referansı
description: Paragraph yöntem. Bu paragrafa bir alan ekler.
type: docs
weight: 260
url: /tr/net/aspose.words/paragraph/appendfield/
---
## AppendField(FieldType, bool) {#appendfield}

Bu paragrafa bir alan ekler.

```csharp
public Field AppendField(FieldType fieldType, bool updateField)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fieldType | FieldType | Eklenecek alanın türü. |
| updateField | Boolean | Alanın hemen güncellenip güncellenmeyeceğini belirtir. |

### Geri dönüş değeri

A[`Field`](../../../aspose.words.fields/field/) eklenen alanı temsil eden nesne.

### Örnekler

Bir paragrafa alan eklemenin çeşitli yollarını gösterir.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Aşağıda paragrafın sonuna alan eklemenin üç yolu verilmiştir.
// 1 - Alan türünü kullanarak bir DATE alanı ekleyin ve ardından güncelleyin:
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 - Alan kodunu kullanarak bir TIME alanı ekleyin:
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - Bir alan kodu kullanarak bir QUOTE alanı ekleyin ve bunun bir yer tutucu değeri görüntülemesini sağlayın:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// Bu alan, biz güncelleyene kadar yer tutucu değerini gösterecektir.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Ayrıca bakınız

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [Paragraph](../)
* ad alanı [Aspose.Words](../../paragraph/)
* toplantı [Aspose.Words](../../../)

---

## AppendField(string) {#appendfield_1}

Bu paragrafa bir alan ekler.

```csharp
public Field AppendField(string fieldCode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fieldCode | String | Eklenecek alan kodu (küme parantezleri olmadan). |

### Geri dönüş değeri

A[`Field`](../../../aspose.words.fields/field/) eklenen alanı temsil eden nesne.

### Örnekler

Bir paragrafa alan eklemenin çeşitli yollarını gösterir.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Aşağıda paragrafın sonuna alan eklemenin üç yolu verilmiştir.
// 1 - Alan türünü kullanarak bir DATE alanı ekleyin ve ardından güncelleyin:
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 - Alan kodunu kullanarak bir TIME alanı ekleyin:
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - Bir alan kodu kullanarak bir QUOTE alanı ekleyin ve bunun bir yer tutucu değeri görüntülemesini sağlayın:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// Bu alan, biz güncelleyene kadar yer tutucu değerini gösterecektir.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Ayrıca bakınız

* class [Field](../../../aspose.words.fields/field/)
* class [Paragraph](../)
* ad alanı [Aspose.Words](../../paragraph/)
* toplantı [Aspose.Words](../../../)

---

## AppendField(string, string) {#appendfield_2}

Bu paragrafa bir alan ekler.

```csharp
public Field AppendField(string fieldCode, string fieldValue)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fieldCode | String | Eklenecek alan kodu (küme parantezleri olmadan). |
| fieldValue | String | Eklenecek alan değeri. Geçmek`hükümsüz` değeri olmayan alanlar için. |

### Geri dönüş değeri

A[`Field`](../../../aspose.words.fields/field/) eklenen alanı temsil eden nesne.

### Örnekler

Bir paragrafa alan eklemenin çeşitli yollarını gösterir.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Aşağıda paragrafın sonuna alan eklemenin üç yolu verilmiştir.
// 1 - Alan türünü kullanarak bir DATE alanı ekleyin ve ardından güncelleyin:
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 - Alan kodunu kullanarak bir TIME alanı ekleyin:
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - Bir alan kodu kullanarak bir QUOTE alanı ekleyin ve bunun bir yer tutucu değeri görüntülemesini sağlayın:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// Bu alan, biz güncelleyene kadar yer tutucu değerini gösterecektir.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Ayrıca bakınız

* class [Field](../../../aspose.words.fields/field/)
* class [Paragraph](../)
* ad alanı [Aspose.Words](../../paragraph/)
* toplantı [Aspose.Words](../../../)


