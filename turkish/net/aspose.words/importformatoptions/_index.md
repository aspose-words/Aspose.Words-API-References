---
title: Class ImportFormatOptions
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.ImportFormatOptions sınıf. Çıktıyı biçimlendirmek için çeşitli içe aktarma seçeneklerinin belirtilmesine olanak tanır.
type: docs
weight: 3240
url: /tr/net/aspose.words/importformatoptions/
---
## ImportFormatOptions class

Çıktıyı biçimlendirmek için çeşitli içe aktarma seçeneklerinin belirtilmesine olanak tanır.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Yükleme Seçeneklerini Belirtin](https://docs.aspose.com/words/net/specify-load-options/) dokümantasyon makalesi.

```csharp
public class ImportFormatOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [ImportFormatOptions](importformatoptions/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AdjustSentenceAndWordSpacing](../../aspose.words/importformatoptions/adjustsentenceandwordspacing/) { get; set; } | Cümle ve kelime aralığının otomatik olarak ayarlanıp ayarlanmayacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değer:`YANLIŞ` . |
| [ForceCopyStyles](../../aspose.words/importformatoptions/forcecopystyles/) { get; set; } | Çakışan stillerin 'nin kopyalanacağını belirten bir boole değeri alır veya ayarlar.KeepSourceFormatting mode. Varsayılan değer:`YANLIŞ` . |
| [IgnoreHeaderFooter](../../aspose.words/importformatoptions/ignoreheaderfooter/) { get; set; } | Üstbilgi/altbilgi içeriğinin kaynak biçimlendirmesinin göz ardı edildiğini belirten bir boole değeri alır veya ayarlar ifKeepSourceFormatting modu kullanılır. Varsayılan değer:`doğru` . |
| [IgnoreTextBoxes](../../aspose.words/importformatoptions/ignoretextboxes/) { get; set; } | Metin kutusu içeriğinin kaynak biçimlendirmesinin göz ardı edildiğini belirten bir boole değeri alır veya ayarlar ifKeepSourceFormatting modu kullanılır. Varsayılan değer:`doğru` . |
| [KeepSourceNumbering](../../aspose.words/importformatoptions/keepsourcenumbering/) { get; set; } | Kaynak ve hedef belgelerde çakıştığında numaralandırmanın nasıl içe aktarılacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değer:`YANLIŞ` . |
| [MergePastedLists](../../aspose.words/importformatoptions/mergepastedlists/) { get; set; } | Yapıştırılan listelerin çevresindeki listelerle birleştirilip birleştirilmeyeceğini belirten bir boole değeri alır veya ayarlar. Varsayılan değer:`YANLIŞ` . |
| [SmartStyleBehavior](../../aspose.words/importformatoptions/smartstylebehavior/) { get; set; } | Kaynak ve hedef belgelerde eşit adlara sahip olduklarında stillerin nasıl içe aktarılacağını belirten bir boole değeri alır veya ayarlar . Varsayılan değer:`YANLIŞ` . |

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


