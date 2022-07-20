---
title: Update
second_title: Aspose.Words for .NET API Referansı
description: Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa atar.
type: docs
weight: 140
url: /tr/net/aspose.words.fields/field/update/
---
## Update() {#update}

Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa atar.

```csharp
public void Update()
```

### Örnekler

FieldType kullanarak bir belgeye nasıl alan ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Oluşturucu eklerken güncellenip güncellenmeyeceğini belirleyen bir bayrak geçerken iki alan ekleyin.
// Bazı durumlarda, alanların güncellenmesi hesaplama açısından pahalı olabilir ve güncellemeyi ertelemek iyi bir fikir olabilir.
doc.BuiltInDocumentProperties.Author = "John Doe";
builder.Write("This document was written by ");
builder.InsertField(FieldType.FieldAuthor, updateInsertedFieldsImmediately);

builder.InsertParagraph();
builder.Write("\nThis is page ");
builder.InsertField(FieldType.FieldPage, updateInsertedFieldsImmediately);

Assert.AreEqual(" AUTHOR ", doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(" PAGE ", doc.Range.Fields[1].GetFieldCode());

if (updateInsertedFieldsImmediately)
{
    Assert.AreEqual("John Doe", doc.Range.Fields[0].Result);
    Assert.AreEqual("1", doc.Range.Fields[1].Result);
}
else
{
    Assert.AreEqual(string.Empty, doc.Range.Fields[0].Result);
    Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);

    // Güncelleme yöntemlerini manuel olarak kullanarak bu alanları güncellememiz gerekecek.
    doc.Range.Fields[0].Update();

    Assert.AreEqual("John Doe", doc.Range.Fields[0].Result);

    doc.UpdateFields();

    Assert.AreEqual("1", doc.Range.Fields[1].Result);
}
```

Alan sonuçlarının nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Biçim uygulanmamış sonucu görüntüleyen bir alan eklemek için bir belge oluşturucu kullanın.
Field field = builder.InsertField("= 2 + 3");

Assert.AreEqual("= 2 + 3", field.GetFieldCode());
Assert.AreEqual("5", field.Result);

// Alanın özelliklerini kullanarak bir alanın sonucuna bir format uygulayabiliriz.
// Aşağıda, bir alanın sonucuna uygulayabileceğimiz üç tür biçim bulunmaktadır.
// 1 - Sayısal biçim:
FieldFormat format = field.Format;
format.NumericFormat = "$###.00";
field.Update();

Assert.AreEqual("= 2 + 3 \\# $###.00", field.GetFieldCode());
Assert.AreEqual("$  5.00", field.Result);

// 2 - Tarih/saat biçimi:
field = builder.InsertField("DATE");
format = field.Format;
format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());
Console.WriteLine($"Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

// 3 - Genel biçim:
field = builder.InsertField("= 25 + 33");
format = field.Format;
format.GeneralFormats.Add(GeneralFormat.LowercaseRoman);
format.GeneralFormats.Add(GeneralFormat.Upper);
field.Update();

int index = 0;
using (IEnumerator<GeneralFormat> generalFormatEnumerator = format.GeneralFormats.GetEnumerator())
    while (generalFormatEnumerator.MoveNext())
        Console.WriteLine($"General format index {index++}: {generalFormatEnumerator.Current}");

Assert.AreEqual("= 25 + 33 \\* roman \\* Upper", field.GetFieldCode());
Assert.AreEqual("LVIII", field.Result);
Assert.AreEqual(2, format.GeneralFormats.Count);
Assert.AreEqual(GeneralFormat.LowercaseRoman, format.GeneralFormats[0]);

// Alanın sonucunu orijinal haline döndürmek için formatlarımızı kaldırabiliriz.
format.GeneralFormats.Remove(GeneralFormat.LowercaseRoman);
format.GeneralFormats.RemoveAt(0);
Assert.AreEqual(0, format.GeneralFormats.Count);
field.Update();

Assert.AreEqual("= 25 + 33  ", field.GetFieldCode());
Assert.AreEqual("58", field.Result);
Assert.AreEqual(0, format.GeneralFormats.Count);
```

### Ayrıca bakınız

* class [Field](../../field)
* ad alanı [Aspose.Words.Fields](../../field)
* toplantı [Aspose.Words](../../../)

---

## Update(bool) {#update_1}

Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa atar.

```csharp
public void Update(bool ignoreMergeFormat)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| ignoreMergeFormat | Boolean | Eğer`doğru` daha sonra MERGEFORMAT anahtarından bağımsız olarak doğrudan alan sonuç biçimlendirmesi terk edilir, aksi takdirde normal güncelleme gerçekleştirilir. |

### Örnekler

Bir belge yüklenirken INCLUDEPICTURE alanlarının nasıl korunacağını veya atılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldIncludePicture includePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
includePicture.SourceFullName = ImageDir + "Transparent background logo.png";
includePicture.Update(true);

using (MemoryStream docStream = new MemoryStream())
{
    doc.Save(docStream, new OoxmlSaveOptions(SaveFormat.Docx));

    // Tüm INCLUDEPICTURE alanlarının dönüştürülüp dönüştürülmeyeceğine karar vermek için LoadOptions nesnesinde bir bayrak ayarlayabiliriz
    // onları içeren bir belge yüklerken görüntü şekillerine.
    LoadOptions loadOptions = new LoadOptions
    {
        PreserveIncludePictureField = preserveIncludePictureField
    };

    doc = new Document(docStream, loadOptions);

    if (preserveIncludePictureField)
    {
        Assert.True(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture));

        doc.UpdateFields();
        doc.Save(ArtifactsDir + "Field.PreserveIncludePicture.docx");
    }
    else
    {
        Assert.False(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture));
    }
}
```

### Ayrıca bakınız

* class [Field](../../field)
* ad alanı [Aspose.Words.Fields](../../field)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
