---
title: ImportFormatOptions.SmartStyleBehavior
second_title: Aspose.Words for .NET API Referansı
description: ImportFormatOptions mülk. Kaynak ve hedef belgelerde eşit adlara sahip olduklarında stillerin nasıl içe aktarılacağını belirten bir boole değeri alır veya ayarlar . Varsayılan değerYANLIŞ .
type: docs
weight: 80
url: /tr/net/aspose.words/importformatoptions/smartstylebehavior/
---
## ImportFormatOptions.SmartStyleBehavior property

Kaynak ve hedef belgelerde eşit adlara sahip olduklarında stillerin nasıl içe aktarılacağını belirten bir boole değeri alır veya ayarlar . Varsayılan değer:`YANLIŞ` .

```csharp
public bool SmartStyleBehavior { get; set; }
```

### Notlar

Bu seçenek olduğunda **etkinleştirilmiş** kaynak stili a hedef belgesinin içindeki doğrudan niteliklere genişletilecektir, eğerKeepSourceFormatting içe aktarma modu kullanılır.

Bu seçenek olduğunda **engelli**kaynak stili yalnızca numaralandırılmışsa genişletilecektir. Listeler dahil, Existing hedef nitelikleri geçersiz kılınmayacak.

### Örnekler

Belgeleri eklerken yinelenen stillerin nasıl çözüleceğini gösterir.

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

Style myStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyStyle");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

// Belgeyi kopyalayın ve kopyanın "MyStyle" stilini düzenleyin, böylece orijinalinden farklı bir renk olur.
// Klonu orijinal belgeye eklersek aynı isimdeki iki stil çakışmaya neden olur.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// SmartStyleBehavior'ı etkinleştirdiğimizde ve KeepSourceFormatting içe aktarma formatı modunu kullandığımızda,
// Aspose.Words, kaynak belge stillerini dönüştürerek stil çakışmalarını çözecektir.
// hedef stillerle aynı adları doğrudan paragraf niteliklerine dönüştürün.
ImportFormatOptions options = new ImportFormatOptions();
options.SmartStyleBehavior = true;

builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.SmartStyleBehavior.docx");
```

### Ayrıca bakınız

* class [ImportFormatOptions](../)
* ad alanı [Aspose.Words](../../importformatoptions/)
* toplantı [Aspose.Words](../../../)


