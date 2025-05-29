---
title: ImportFormatOptions.SmartStyleBehavior
linktitle: SmartStyleBehavior
articleTitle: SmartStyleBehavior
second_title: .NET için Aspose.Words
description: ImportFormatOptions SmartStyleBehavior özelliğinin belgelerdeki eşit adlarla stil içe aktarımlarını nasıl optimize ettiğini keşfedin. İçe aktarma sürecinizi zahmetsizce özelleştirin!
type: docs
weight: 80
url: /tr/net/aspose.words/importformatoptions/smartstylebehavior/
---
## ImportFormatOptions.SmartStyleBehavior property

Kaynak ve hedef belgelerde eşit adlara sahip olduklarında stillerin nasıl içe aktarılacağını belirten bir Boole değeri alır veya ayarlar. Varsayılan değer`YANLIŞ` .

```csharp
public bool SmartStyleBehavior { get; set; }
```

## Notlar

Bu seçenek olduğunda**etkinleştirilmiş** , kaynak stili, a hedef belgesinin içindeki doğrudan özniteliklere genişletilecektir, eğerKeepSourceFormatting içe aktarma modu kullanılıyor.

Bu seçenek olduğunda**engelli**, kaynak stili yalnızca numaralandırılırsa genişletilecektir. Mevcut hedef öznitelikleri, listeler dahil olmak üzere geçersiz kılınmayacaktır.

## Örnekler

Belgeler eklenirken yinelenen stillerin nasıl çözüleceğini gösterir.

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

Style myStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyStyle");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

// Belgeyi klonlayın ve klonun "MyStyle" stilini düzenleyin, böylece orijinalinden farklı bir renge sahip olur.
// Klonu orijinal belgeye eklersek, aynı ada sahip iki stil çakışmaya neden olur.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// SmartStyleBehavior'ı etkinleştirdiğimizde ve KeepSourceFormatting içe aktarma biçim modunu kullandığımızda,
// Aspose.Words, kaynak belge stillerini dönüştürerek stil çakışmalarını çözecektir.
// hedef stillerle aynı adları doğrudan paragraf özniteliklerine aktarın.
ImportFormatOptions options = new ImportFormatOptions();
options.SmartStyleBehavior = true;

builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.SmartStyleBehavior.docx");
```

### Ayrıca bakınız

* class [ImportFormatOptions](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
