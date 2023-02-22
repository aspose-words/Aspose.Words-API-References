---
title: Font.Bidi
second_title: Aspose.Words for .NET API Referansı
description: Font mülk. Bu çalıştırmanın içeriğinin sağdan sola özelliklere sahip olup olmayacağını belirtir.
type: docs
weight: 30
url: /tr/net/aspose.words/font/bidi/
---
## Font.Bidi property

Bu çalıştırmanın içeriğinin sağdan sola özelliklere sahip olup olmayacağını belirtir.

```csharp
public bool Bidi { get; set; }
```

### Notlar

Bu özellik, açık olduğunda, soldan sağa güçlü metinlerle kullanılmamalıdır. Bu koşul altındaki herhangi bir davranış belirtilmemiştir. Bu özellik kapalıyken, sağdan sola yazılan güçlü metinlerle kullanılmamalıdır. Bu koşul altındaki herhangi bir davranış belirtilmemiştir.

Bu çalıştırmanın içeriği görüntülendiğinde, tüm karakterler, biçimlendirme amaçları için karmaşık komut dosyası karakterleri olarak ele alınacaktır. Bunun anlamı şudur ki[`BoldBi`](../boldbi/) ,[`ItalicBi`](../italicbi/) ,[`SizeBi`](../sizebi/) ve bu çalıştırmayı oluştururken karşılık gelen bir font name kullanılacaktır.

Ayrıca, bu çalıştırmanın içeriği görüntülendiğinde, bu özellik "zayıf türler" ve "nötr türler" olarak sınıflandırılan karakterler için sağdan sola geçersiz kılma işlevi görür.

### Örnekler

Sağdan sola ve sağdan sola metin için ayrı yazı tipi ayarları kümelerinin nasıl tanımlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Soldan sağa metin için bir dizi yazı tipi ayarı tanımlayın.
builder.Font.Name = "Courier New";
builder.Font.Size = 16;
builder.Font.Italic = false;
builder.Font.Bold = false;
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Sağdan sola metin için başka bir yazı tipi ayarları kümesi tanımlayın.
builder.Font.NameBi = "Andalus";
builder.Font.SizeBi = 24;
builder.Font.ItalicBi = true;
builder.Font.BoldBi = true;
builder.Font.LocaleIdBi = new CultureInfo("ar-AR", false).LCID;

// Eklemek üzere olduğumuz metnin olup olmadığını belirtmek için Bidi bayrağını kullanabiliriz
// belge oluşturucu ile sağdan sola. Bu bayrak true olarak ayarlanmış şekilde metin eklediğimizde,
// sağdan sola yazı tipi ayarları kümesi kullanılarak biçimlendirilecektir.
builder.Font.Bidi = true;
builder.Write("مرحبًا");

// Bayrağı false olarak ayarlayın ve ardından soldan sağa metin ekleyin.
// Belge oluşturucu, bunları soldan sağa yazı tipi ayarları kümesini kullanarak biçimlendirir.
builder.Font.Bidi = false;
builder.Write(" Hello world!");

doc.Save(ArtifactsDir + "Font.Bidi.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../font/)
* toplantı [Aspose.Words](../../../)


