---
title: Style.Remove
second_title: Aspose.Words for .NET API Referansı
description: Style yöntem. Belirtilen stili belgeden kaldırır.
type: docs
weight: 200
url: /tr/net/aspose.words/style/remove/
---
## Style.Remove method

Belirtilen stili belgeden kaldırır.

```csharp
public void Remove()
```

### Notlar

Stil kaldırmanın belge modeli üzerinde aşağıdaki etkileri vardır:

* Stile yapılan tüm referanslar ilgili paragraflardan, satırlardan ve tablolardan kaldırılır.
* Temel stil kaldırılırsa biçimlendirmesi alt stillere taşınır.
* Silinecek stilin bağlantılı bir stili varsa her ikisi de silinir.

### Örnekler

Özel bir stilin nasıl oluşturulacağını ve uygulanacağını gösterir.

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;
// Stili otomatik olarak yeniden tanımlayın.
style.AutomaticallyUpdate = true;

DocumentBuilder builder = new DocumentBuilder(doc);

// Belgedeki stillerden birini belge oluşturucunun oluşturduğu paragrafa uygulayın.
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// Özel stilimizi belgenin stil koleksiyonundan kaldırın.
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// Kaldırılmış bir stil kullanan herhangi bir metin, varsayılan biçimlendirmeye geri döner.
Assert.False(doc.Styles.Any(s => s.Name == "MyStyle"));
Assert.AreEqual("Times New Roman", firstParagraphStyle.Font.Name);
Assert.AreEqual(12.0d, firstParagraphStyle.Font.Size);
Assert.AreEqual(Color.Empty.ToArgb(), firstParagraphStyle.Font.Color.ToArgb());
```

### Ayrıca bakınız

* class [Style](../)
* ad alanı [Aspose.Words](../../style/)
* toplantı [Aspose.Words](../../../)


