---
title: Font.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words for .NET
description: Font Bidi mülk. Bu çalıştırmanın içeriğinin sağdan sola özelliklerine sahip olup olmayacağını belirtir C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words/font/bidi/
---
## Font.Bidi property

Bu çalıştırmanın içeriğinin sağdan sola özelliklerine sahip olup olmayacağını belirtir.

```csharp
public bool Bidi { get; set; }
```

## Notlar

Bu özellik açıkken soldan sağa güçlü metinlerle kullanılmayacaktır. Bu koşul altında herhangi bir davranış belirtilmemiştir. Bu özellik kapalıyken sağdan sola güçlü metinlerle kullanılmayacaktır. Bu koşul altındaki herhangi bir davranış belirtilmemiştir.

Bu çalıştırmanın içeriği görüntülendiğinde, tüm karakterler, biçimlendirme amacıyla karmaşık komut dosyası karakterleri olarak ele alınacaktır. Bu şu demek[`BoldBi`](../boldbi/) ,[`ItalicBi`](../italicbi/) ,[`SizeBi`](../sizebi/) ve bu çalıştırma oluşturulurken buna karşılık gelen name yazı tipi kullanılacaktır.

Ayrıca, bu çalıştırmanın içeriği görüntülendiğinde bu özellik, "zayıf türler" ve "nötr türler" olarak sınıflandırılan karakterler için sağdan sola geçersiz kılma işlevi görür.

## Örnekler

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

// Eklemek üzere olduğumuz metnin olup olmadığını belirtmek için Bidi bayrağını kullanabiliriz.
// belge oluşturucu ile sağdan soladır. Bu bayrak true olarak ayarlanmış şekilde metin eklediğimizde,
// sağdan sola yazı tipi ayarları kullanılarak biçimlendirilecektir.
builder.Font.Bidi = true;
builder.Write("مرحبًا");

// Bayrağı false olarak ayarlayın ve ardından soldan sağa metni ekleyin.
// Belge oluşturucu bunları soldan sağa yazı tipi ayarlarını kullanarak biçimlendirecektir.
builder.Font.Bidi = false;
builder.Write(" Hello world!");

doc.Save(ArtifactsDir + "Font.Bidi.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
