---
title: Class ImportFormatOptions
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.ImportFormatOptions sınıf. Çıktıyı biçimlendirmek için çeşitli içe aktarma seçeneklerinin belirlenmesine izin verir.
type: docs
weight: 3040
url: /tr/net/aspose.words/importformatoptions/
---
## ImportFormatOptions class

Çıktıyı biçimlendirmek için çeşitli içe aktarma seçeneklerinin belirlenmesine izin verir.

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
| [ForceCopyStyles](../../aspose.words/importformatoptions/forcecopystyles/) { get; set; } | Bir boole değeri alır veya ayarlar.KeepSourceFormatting mode. Varsayılan değer`yanlış` . |
| [IgnoreHeaderFooter](../../aspose.words/importformatoptions/ignoreheaderfooter/) { get; set; } | Üstbilgi/altbilgi içeriğinin kaynak biçimlendirmesinin yoksayıldığını belirten bir boole değeri alır veya ayarlar.KeepSourceFormatting modu kullanılır. Varsayılan değer`doğru` . |
| [IgnoreTextBoxes](../../aspose.words/importformatoptions/ignoretextboxes/) { get; set; } | Metin kutuları içeriğinin kaynak biçimlendirmesinin yoksayıldığını belirten bir boole değeri alır veya ayarlar.KeepSourceFormatting modu kullanılır. Varsayılan değer`doğru` . |
| [KeepSourceNumbering](../../aspose.words/importformatoptions/keepsourcenumbering/) { get; set; } | Kaynak ve hedef belgelerde çakıştığında numaralandırmanın nasıl içe aktarılacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değer`yanlış` . |
| [MergePastedLists](../../aspose.words/importformatoptions/mergepastedlists/) { get; set; } | Yapıştırılan listelerin çevredeki listelerle birleştirilip birleştirilmeyeceğini belirten bir boole değeri alır veya ayarlar. Varsayılan değer`yanlış` . |
| [SmartStyleBehavior](../../aspose.words/importformatoptions/smartstylebehavior/) { get; set; } | Kaynak ve hedef belgelerde eşit ada sahip olduklarında stillerin nasıl içe aktarılacağını belirten bir boole değeri alır veya ayarlar . Varsayılan değer`yanlış` . |

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


