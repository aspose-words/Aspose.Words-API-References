---
title: Style.AutomaticallyUpdate
linktitle: AutomaticallyUpdate
articleTitle: AutomaticallyUpdate
second_title: Aspose.Words for .NET
description: Style AutomaticallyUpdate mülk. Bu stilin uygun değere göre otomatik olarak yeniden tanımlanıp tanımlanmayacağını belirtir C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words/style/automaticallyupdate/
---
## Style.AutomaticallyUpdate property

Bu stilin uygun değere göre otomatik olarak yeniden tanımlanıp tanımlanmayacağını belirtir.

```csharp
public bool AutomaticallyUpdate { get; set; }
```

## Notlar

Özellik değeri true olarak ayarlanırsa, uygun paragraf formatı değiştirildiğinde MS Word geçerli stili otomatik olarak yeniden tanımlar.

Otomatik Güncelleme özelliği yalnızca paragraf stillerine uygulanabilir.

Varsayılan değer:`YANLIŞ`.

## Örnekler

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
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
