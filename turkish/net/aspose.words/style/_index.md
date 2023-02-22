---
title: Class Style
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Style sınıf. Tek bir yerleşik veya kullanıcı tanımlı stili temsil eder.
type: docs
weight: 5830
url: /tr/net/aspose.words/style/
---
## Style class

Tek bir yerleşik veya kullanıcı tanımlı stili temsil eder.

```csharp
public class Style
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Aliases](../../aspose.words/style/aliases/) { get; } | Bu stilin tüm diğer adlarını alır. Stilin takma adı yoksa, boş dize dizisi döndürülür. |
| [BaseStyleName](../../aspose.words/style/basestylename/) { get; set; } | Bu stilin dayandığı stilin adını alır/ayarlar. |
| [BuiltIn](../../aspose.words/style/builtin/) { get; } | Bu stil MS Word'deki yerleşik stillerden biriyse doğrudur. |
| [Document](../../aspose.words/style/document/) { get; } | Sahip belgesini alır. |
| [Font](../../aspose.words/style/font/) { get; } | Stilin karakter biçimlendirmesini alır. |
| [IsHeading](../../aspose.words/style/isheading/) { get; } | Stil, yerleşik Başlık stillerinden biri olduğunda doğrudur. |
| [IsQuickStyle](../../aspose.words/style/isquickstyle/) { get; set; } | Bu stilin MS Word UI içindeki Hızlı Stil galerisinde gösterilip gösterilmeyeceğini belirtir. |
| [LinkedStyleName](../../aspose.words/style/linkedstylename/) { get; } | Buna bağlı Stilin adını alır. Hiçbir stil bağlı değilse Boş dize döndürür. |
| [List](../../aspose.words/style/list/) { get; } | Bu liste stilinin biçimlendirmesini tanımlayan listeyi alır. |
| [ListFormat](../../aspose.words/style/listformat/) { get; } | Paragraf stilinin liste biçimlendirme özelliklerine erişim sağlar. |
| [Name](../../aspose.words/style/name/) { get; set; } | Stilin adını alır veya ayarlar. |
| [NextParagraphStyleName](../../aspose.words/style/nextparagraphstylename/) { get; set; } | Belirtilen stille biçimlendirilmiş a paragrafından sonra eklenen yeni paragrafa otomatik olarak uygulanacak stilin adını alır/ayarlar. |
| [ParagraphFormat](../../aspose.words/style/paragraphformat/) { get; } | Stilin paragraf biçimlendirmesini alır. |
| [StyleIdentifier](../../aspose.words/style/styleidentifier/) { get; } | Yerleşik bir stil için yerel ayardan bağımsız stil tanımlayıcısını alır. |
| [Styles](../../aspose.words/style/styles/) { get; } | Bu stilin ait olduğu stiller koleksiyonunu alır. |
| [Type](../../aspose.words/style/type/) { get; } | Stil türünü (paragraf veya karakter) alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Equals](../../aspose.words/style/equals/#equals)(Style) | Belirtilen stille karşılaştırır. Stiller İstd'ler yalnızca yerleşik stiller için karşılaştırılır. Stil varsayılanları karşılaştırmaya dahil edilmez. Temel stil, bağlantılı stil ve sonraki paragraf stili yinelemeli olarak karşılaştırılır. |
| [Remove](../../aspose.words/style/remove/)() | Belirtilen stili belgeden kaldırır. |

### Örnekler

Liste biçimlendirmeli bir paragraf stilinin nasıl oluşturulacağını ve kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Özel bir paragraf stili oluşturun.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Bir liste oluşturun ve bu stili kullanan paragrafların bu listeyi kullanacağından emin olun.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Paragraf stilini belge oluşturucunun geçerli paragrafına uygulayın ve ardından biraz metin ekleyin.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Belge oluşturucunun stilini liste biçimlendirmesi olmayan bir stille değiştirin ve başka bir paragraf yazın.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

Özel bir stilin nasıl oluşturulacağını ve uygulanacağını gösterir.

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;

DocumentBuilder builder = new DocumentBuilder(doc);

// Belgedeki stillerden birini belge oluşturucunun oluşturduğu paragrafa uygulayın.
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// Özel stilimizi belgenin stiller koleksiyonundan kaldırın.
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// Kaldırılan bir stil kullanan herhangi bir metin, varsayılan biçimlendirmeye geri döner.
Assert.False(doc.Styles.Any(s => s.Name == "MyStyle"));
Assert.AreEqual("Times New Roman", firstParagraphStyle.Font.Name);
Assert.AreEqual(12.0d, firstParagraphStyle.Font.Size);
Assert.AreEqual(Color.Empty.ToArgb(), firstParagraphStyle.Font.Color.ToArgb());
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


