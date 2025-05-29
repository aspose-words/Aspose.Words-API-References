---
title: ImportFormatOptions Class
linktitle: ImportFormatOptions
articleTitle: ImportFormatOptions
second_title: .NET için Aspose.Words
description: Özelleştirilebilir belge biçimlendirmesi için Aspose.Words.ImportFormatOptions'ı keşfedin. En iyi sonuçlar için özelleştirilmiş içe aktarma ayarlarıyla çıktınızı geliştirin.
type: docs
weight: 3690
url: /tr/net/aspose.words/importformatoptions/
---
## ImportFormatOptions class

Çıktıyı biçimlendirmek için çeşitli içe aktarma seçeneklerinin belirtilmesine olanak tanır.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yükleme Seçeneklerini Belirleyin](https://docs.aspose.com/words/net/specify-load-options/) belgeleme makalesi.

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
| [AdjustSentenceAndWordSpacing](../../aspose.words/importformatoptions/adjustsentenceandwordspacing/) { get; set; } | Cümle ve kelime aralıklarının otomatik olarak ayarlanıp ayarlanamayacağını belirten bir Boole değeri alır veya ayarlar. Varsayılan değer`YANLIŞ` . |
| [ForceCopyStyles](../../aspose.words/importformatoptions/forcecopystyles/) { get; set; } | Çakışan styles 'yi kopyalamak için bir Boole değeri alır veya ayarlar.KeepSourceFormatting mode. Varsayılan değer`YANLIŞ` . |
| [IgnoreHeaderFooter](../../aspose.words/importformatoptions/ignoreheaderfooter/) { get; set; } | Başlık/altbilgi içeriğinin kaynak biçimlendirmesinin yoksayıldığını belirten bir Boole değeri alır veya ayarlar eğerKeepSourceFormatting mod kullanılır. Varsayılan değer`doğru` . |
| [IgnoreTextBoxes](../../aspose.words/importformatoptions/ignoretextboxes/) { get; set; } | Metin kutusu içeriğinin kaynak biçimlendirmesinin yoksayıldığını belirten bir Boole değeri alır veya ayarlar eğerKeepSourceFormatting mod kullanılır. Varsayılan değer`doğru` . |
| [KeepSourceNumbering](../../aspose.words/importformatoptions/keepsourcenumbering/) { get; set; } | Kaynak ve hedef belgelerde çakışma olduğunda numaralandırmanın nasıl içe aktarılacağını belirten bir Boole değeri alır veya ayarlar. Varsayılan değer`YANLIŞ` . |
| [MergePastedLists](../../aspose.words/importformatoptions/mergepastedlists/) { get; set; } | Yapıştırılan listelerin çevreleyen listelerle birleştirilip birleştirilmeyeceğini belirten bir Boole değeri alır veya ayarlar. Varsayılan değer`YANLIŞ` . |
| [SmartStyleBehavior](../../aspose.words/importformatoptions/smartstylebehavior/) { get; set; } | Kaynak ve hedef belgelerde eşit adlara sahip olduklarında stillerin nasıl içe aktarılacağını belirten bir Boole değeri alır veya ayarlar. Varsayılan değer`YANLIŞ` . |

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
