---
title: ImportFormatOptions.SmartStyleBehavior
second_title: Aspose.Words for .NET API Referansı
description: ImportFormatOptions mülk. Kaynak ve hedef belgelerde eşit ada sahip olduklarında stillerin nasıl içe aktarılacağını belirten bir boole değeri alır veya ayarlar . Varsayılan değeryanlış .
type: docs
weight: 70
url: /tr/net/aspose.words/importformatoptions/smartstylebehavior/
---
## ImportFormatOptions.SmartStyleBehavior property

Kaynak ve hedef belgelerde eşit ada sahip olduklarında stillerin nasıl içe aktarılacağını belirten bir boole değeri alır veya ayarlar . Varsayılan değer`yanlış` .

```csharp
public bool SmartStyleBehavior { get; set; }
```

### Notlar

Bu seçenek ne zaman **etkinleştirilmiş** , kaynak stil, aşağıdaki durumlarda a hedef belge içindeki doğrudan niteliklere genişletilecektir:KeepSourceFormatting içe aktarma modu kullanılır.

Bu seçenek ne zaman **engelli**, kaynak stil yalnızca numaralandırılmışsa genişletilecektir. Listeler dahil olmak üzere, mevcut hedef öznitelikleri geçersiz kılınmayacaktır.

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

// Belgeyi klonlayın ve klonun "MyStyle" stilini düzenleyin, böylece orijinalden farklı bir renk olur.
// Klonu orijinal belgeye eklersek, aynı ada sahip iki stil çakışmaya neden olur.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// SmartStyleBehavior'ı etkinleştirdiğimizde ve KeepSourceFormatting içe aktarma biçimi modunu kullandığımızda,
// Aspose.Words, kaynak belge stillerini dönüştürerek stil çakışmalarını çözecektir.
// doğrudan paragraf niteliklerine hedef stiller ile aynı adlarla.
ImportFormatOptions options = new ImportFormatOptions();
options.SmartStyleBehavior = true;

builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.SmartStyleBehavior.docx");
```

### Ayrıca bakınız

* class [ImportFormatOptions](../)
* ad alanı [Aspose.Words](../../importformatoptions/)
* toplantı [Aspose.Words](../../../)


