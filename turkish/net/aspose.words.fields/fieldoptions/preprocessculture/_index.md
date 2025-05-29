---
title: FieldOptions.PreProcessCulture
linktitle: PreProcessCulture
articleTitle: PreProcessCulture
second_title: .NET için Aspose.Words
description: FieldOptions PreProcessCulture'ın, daha iyi doğruluk ve verimlilik için alan değer kültürlerini özelleştirerek veri işleme sürecinizi nasıl geliştirdiğini keşfedin.
type: docs
weight: 170
url: /tr/net/aspose.words.fields/fieldoptions/preprocessculture/
---
## FieldOptions.PreProcessCulture property

Alan değerlerini ön işleme tabi tutmak için kültürü alır veya ayarlar.

```csharp
public CultureInfo PreProcessCulture { get; set; }
```

## Notlar

Şu anda bu özellik yalnızca değerini etkiliyor[`FieldDocProperty`](../../fielddocproperty/) alan.

Varsayılan değer:`hükümsüz` Bu özellik şu şekilde ayarlandığında:`hükümsüz` ,[`FieldDocProperty`](../../fielddocproperty/) alanın değeri, kültür tarafından kontrol edilen preprocessed 'dir.[`FieldUpdateCultureSource`](../fieldupdateculturesource/) mülk.

## Örnekler

Önişleme kültürünün nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Bazı alanların görüntülenen değerlerini biçimlendireceği kültürü ayarlayın.
doc.FieldOptions.PreProcessCulture = new CultureInfo("de-DE");

Field field = builder.InsertField(" DOCPROPERTY CreateTime");

// DOCPROPERTY alanı, sonucunu ön işleme kültürüne göre biçimlendirilmiş olarak görüntüler
// Almanca olarak ayarladık. Alan, "gg.aa.yyyy ss:dd" biçimini kullanarak tarih/saati görüntüleyecektir.
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[.]\d{2}[.]\d{4} \d{2}[:]\d{2}").Success);

doc.FieldOptions.PreProcessCulture = CultureInfo.InvariantCulture;
field.Update();

// Değişmez kültüre geçildikten sonra DOCPROPERTY alanı "mm/dd/yyyy ss:dd" formatını kullanacaktır.
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[/]\d{2}[/]\d{4} \d{2}[:]\d{2}").Success);
```

### Ayrıca bakınız

* class [FieldOptions](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
