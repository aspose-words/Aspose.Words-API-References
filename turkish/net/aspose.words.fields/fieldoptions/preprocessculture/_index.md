---
title: FieldOptions.PreProcessCulture
second_title: Aspose.Words for .NET API Referansı
description: FieldOptions mülk. Alan değerlerini ön işlemek için kültürü alır veya ayarlar.
type: docs
weight: 170
url: /tr/net/aspose.words.fields/fieldoptions/preprocessculture/
---
## FieldOptions.PreProcessCulture property

Alan değerlerini ön işlemek için kültürü alır veya ayarlar.

```csharp
public CultureInfo PreProcessCulture { get; set; }
```

### Notlar

Şu anda bu özellik yalnızca[`FieldDocProperty`](../../fielddocproperty/) alan.

Varsayılan değer:`hükümsüz` . Bu özellik olarak ayarlandığında`hükümsüz` ,[`FieldDocProperty`](../../fielddocproperty/)alanın değeri, kültür tarafından kontrol edilen preprocessed 'dir.[`FieldUpdateCultureSource`](../fieldupdateculturesource/) mülk.

### Örnekler

Önişleme kültürünün nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Bazı alanların görüntülenen değerlerini buna göre biçimlendireceği kültürü ayarlayın.
doc.FieldOptions.PreProcessCulture = new CultureInfo("de-DE");

Field field = builder.InsertField(" DOCPROPERTY CreateTime");

// DOCPROPERTY alanı, önişleme kültürüne göre biçimlendirilmiş sonucunu görüntüleyecektir
// Almancayı ayarladık. Alan, "dd.mm.yyyy ss:dd" biçimini kullanarak tarih/saati görüntüler.
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[.]\d{2}[.]\d{4} \d{2}[:]\d{2}").Success);

doc.FieldOptions.PreProcessCulture = CultureInfo.InvariantCulture;
field.Update();

// Değişmez kültüre geçtikten sonra DOCPROPERTY alanı "aa/gg/yyyy ss:dd" biçimini kullanacaktır.
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[/]\d{2}[/]\d{4} \d{2}[:]\d{2}").Success);
```

### Ayrıca bakınız

* class [FieldOptions](../)
* ad alanı [Aspose.Words.Fields](../../fieldoptions/)
* toplantı [Aspose.Words](../../../)


