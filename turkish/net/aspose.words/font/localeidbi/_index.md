---
title: Font.LocaleIdBi
second_title: Aspose.Words for .NET API Referansı
description: Font mülk. Biçimlendirilmiş sağdan sola karakterlerin yerel ayar tanımlayıcısını dili alır veya ayarlar.
type: docs
weight: 210
url: /tr/net/aspose.words/font/localeidbi/
---
## Font.LocaleIdBi property

Biçimlendirilmiş sağdan sola karakterlerin yerel ayar tanımlayıcısını (dili) alır veya ayarlar.

```csharp
public int LocaleIdBi { get; set; }
```

### Notlar

Yerel tanımlayıcıların listesi için bkz. https://msdn.microsoft.com/en-us/library/cc233965.aspx

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
* ad alanı [Aspose.Words](../../font/)
* toplantı [Aspose.Words](../../../)


