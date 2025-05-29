---
title: Font Class
linktitle: Font
articleTitle: Font
second_title: .NET için Aspose.Words
description: Belgenizin biçimlendirmesini ve tasarımını geliştirmek için ad, boyut ve renk gibi temel yazı tipi niteliklerini içeren Aspose.Words.Font sınıfını keşfedin.
type: docs
weight: 3240
url: /tr/net/aspose.words/font/
---
## Font class

Bir nesne için yazı tipi niteliklerini (yazı tipi adı, yazı tipi boyutu, renk vb.) içerir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yazı Tipleriyle Çalışma](https://docs.aspose.com/words/net/working-with-fonts/) belgeleme makalesi.

```csharp
public class Font
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AllCaps](../../aspose.words/font/allcaps/) { get; set; } | Yazı tipi tamamen büyük harf olarak biçimlendirilmişse doğrudur. |
| [AutoColor](../../aspose.words/font/autocolor/) { get; } | 'otomatik renk' için kullanılacak metnin (siyah veya beyaz) mevcut hesaplanmış rengini döndürür. Renk 'otomatik' değilse, o zaman şunu döndürür:[`Color`](./color/) . |
| [Bidi](../../aspose.words/font/bidi/) { get; set; } | Bu çalışmanın içeriğinin sağdan sola özelliklere sahip olup olmayacağını belirtir. |
| [Bold](../../aspose.words/font/bold/) { get; set; } | Yazı tipi kalın olarak biçimlendirilmişse doğrudur. |
| [BoldBi](../../aspose.words/font/boldbi/) { get; set; } | Sağdan sola metin kalın olarak biçimlendirilirse doğrudur. |
| [Border](../../aspose.words/font/border/) { get; } | Bir[`Border`](../border/) yazı tipi için kenarlığı belirten nesne. |
| [Color](../../aspose.words/font/color/) { get; set; } | Yazı tipinin rengini alır veya ayarlar. |
| [ComplexScript](../../aspose.words/font/complexscript/) { get; set; } | Bu çalışmanın içeriğinin, bu çalışmanın biçimlendirmesini belirlerken Unicode karakter değerlerinden bağımsız olarak karmaşık betik metni olarak ele alınıp alınmayacağını belirtir. |
| [DoubleStrikeThrough](../../aspose.words/font/doublestrikethrough/) { get; set; } | Yazı tipi çift üstü çizili metin olarak biçimlendirilmişse doğrudur. |
| [Emboss](../../aspose.words/font/emboss/) { get; set; } | Yazı tipi kabartmalı olarak biçimlendirilmişse doğrudur. |
| [EmphasisMark](../../aspose.words/font/emphasismark/) { get; set; } | Bu biçimlendirmeye uygulanan vurgu işaretini alır veya ayarlar. |
| [Engrave](../../aspose.words/font/engrave/) { get; set; } | Yazı tipi oyulmuş olarak biçimlendirilmişse doğrudur. |
| [Fill](../../aspose.words/font/fill/) { get; } | için doldurma biçimlendirmesini alır`Font` . |
| [Hidden](../../aspose.words/font/hidden/) { get; set; } | Yazı tipi gizli metin olarak biçimlendirilmişse doğrudur. |
| [HighlightColor](../../aspose.words/font/highlightcolor/) { get; set; } | Vurgu (işaretleyici) rengini alır veya ayarlar. |
| [Italic](../../aspose.words/font/italic/) { get; set; } | Yazı tipi italik olarak biçimlendirilmişse doğrudur. |
| [ItalicBi](../../aspose.words/font/italicbi/) { get; set; } | Sağdan sola metin italik olarak biçimlendirilmişse doğrudur. |
| [Kerning](../../aspose.words/font/kerning/) { get; set; } | Kerning'in başlayacağı yazı tipi boyutunu alır veya ayarlar. |
| [LineSpacing](../../aspose.words/font/linespacing/) { get; } | Bu yazı tipinin satır aralığını (nokta cinsinden) döndürür. |
| [LocaleId](../../aspose.words/font/localeid/) { get; set; } | Biçimlendirilmiş karakterlerin yerel tanımlayıcısını (dil) alır veya ayarlar. |
| [LocaleIdBi](../../aspose.words/font/localeidbi/) { get; set; } | Biçimlendirilmiş sağdan sola karakterlerin yerel tanımlayıcısını (dil) alır veya ayarlar. |
| [LocaleIdFarEast](../../aspose.words/font/localeidfareast/) { get; set; } | Biçimlendirilmiş Asya karakterlerinin yerel tanımlayıcısını (dil) alır veya ayarlar. |
| [Name](../../aspose.words/font/name/) { get; set; } | Yazı tipinin adını alır veya ayarlar. |
| [NameAscii](../../aspose.words/font/nameascii/) { get; set; } | Latin metinleri için kullanılan yazı tipini döndürür veya ayarlar (karakter kodları 0 (sıfır) ile 127 arasında olan karakterler). |
| [NameBi](../../aspose.words/font/namebi/) { get; set; } | Sağdan sola dil belgesindeki yazı tipinin adını döndürür veya ayarlar. |
| [NameFarEast](../../aspose.words/font/namefareast/) { get; set; } | Doğu Asya yazı tipi adını döndürür veya ayarlar. |
| [NameOther](../../aspose.words/font/nameother/) { get; set; } | 128 ile 255 arasındaki karakter kodlarına sahip karakterler için kullanılan yazı tipini döndürür veya ayarlar. |
| [NoProofing](../../aspose.words/font/noproofing/) { get; set; } | Biçimlendirilmiş karakterlerin yazım denetimi yapılmayacaksa doğrudur. |
| [NumberSpacing](../../aspose.words/font/numberspacing/) { get; set; } | Görüntülenen rakamın aralık türünü alır veya ayarlar. |
| [Outline](../../aspose.words/font/outline/) { get; set; } | Yazı tipi anahat olarak biçimlendirilmişse doğrudur. |
| [Position](../../aspose.words/font/position/) { get; set; } | Metnin taban çizgisine göre konumunu (nokta cinsinden) alır veya ayarlar. Pozitif bir sayı metni yükseltir ve negatif bir sayı düşürür. |
| [Scaling](../../aspose.words/font/scaling/) { get; set; } | Karakter genişliği ölçeklemesini yüzde olarak alır veya ayarlar. |
| [Shading](../../aspose.words/font/shading/) { get; } | Bir[`Shading`](../shading/) yazı tipinin gölgelendirme biçimlendirmesine başvuran nesne. |
| [Shadow](../../aspose.words/font/shadow/) { get; set; } | Yazı tipi gölgeli olarak biçimlendirilmişse doğrudur. |
| [Size](../../aspose.words/font/size/) { get; set; } | Yazı tipi boyutunu nokta cinsinden alır veya ayarlar. |
| [SizeBi](../../aspose.words/font/sizebi/) { get; set; } | Sağdan sola bir belgede kullanılan yazı tipi boyutunu noktalar halinde alır veya ayarlar. |
| [SmallCaps](../../aspose.words/font/smallcaps/) { get; set; } | Yazı tipi küçük büyük harflerle biçimlendirilmişse doğrudur. |
| [SnapToGrid](../../aspose.words/font/snaptogrid/) { get; set; } | Geçerli yazı tipinin düzenlenme sırasında satır başına belge ızgara karakterleri ayarlarını kullanıp kullanmayacağını belirtir. |
| [Spacing](../../aspose.words/font/spacing/) { get; set; } | Karakterler arasındaki boşluğu (nokta cinsinden) döndürür veya ayarlar. |
| [StrikeThrough](../../aspose.words/font/strikethrough/) { get; set; } | Yazı tipi üstü çizili metin olarak biçimlendirilmişse doğrudur. |
| [Style](../../aspose.words/font/style/) { get; set; } | Bu biçimlendirmeye uygulanan karakter stilini alır veya ayarlar. |
| [StyleIdentifier](../../aspose.words/font/styleidentifier/) { get; set; } | Bu biçimlendirmeye uygulanan karakter stilinin yerel bağımsız stil tanımlayıcısını alır veya ayarlar. |
| [StyleName](../../aspose.words/font/stylename/) { get; set; } | Bu biçimlendirmeye uygulanan karakter stilinin adını alır veya ayarlar. |
| [Subscript](../../aspose.words/font/subscript/) { get; set; } | Yazı tipi alt simge olarak biçimlendirilmişse doğrudur. |
| [Superscript](../../aspose.words/font/superscript/) { get; set; } | Yazı tipi üst simge olarak biçimlendirilmişse doğrudur. |
| [TextEffect](../../aspose.words/font/texteffect/) { get; set; } | Yazı tipi animasyon efektini alır veya ayarlar. |
| [ThemeColor](../../aspose.words/font/themecolor/) { get; set; } | Bu temayla ilişkili uygulanan renk şemasındaki tema rengini alır veya ayarlar`Font` nesne. |
| [ThemeFont](../../aspose.words/font/themefont/) { get; set; } | Bu temayla ilişkili uygulanan yazı tipi şemasındaki tema yazı tipini alır veya ayarlar`Font` nesne. |
| [ThemeFontAscii](../../aspose.words/font/themefontascii/) { get; set; } | Latin metni için kullanılan tema yazı tipini alır veya ayarlar (karakter kodları 0 (sıfır) ile 127 arasında olan karakterler) bu uygulamayla ilişkili olan yazı tipi şemasında`Font` nesne. |
| [ThemeFontBi](../../aspose.words/font/themefontbi/) { get; set; } | Bu temayla ilişkili uygulanan yazı tipi şemasındaki tema yazı tipini alır veya ayarlar`Font` Sağdan sola dil belgesinde object |
| [ThemeFontFarEast](../../aspose.words/font/themefontfareast/) { get; set; } | Bu temayla ilişkili uygulanan yazı tipi şemasındaki Doğu Asya tema yazı tipini alır veya ayarlar`Font` nesne. |
| [ThemeFontOther](../../aspose.words/font/themefontother/) { get; set; } | Bu uygulamayla ilişkili yazı tipi şemasında 128'den 255'e kadar karakter kodlarına sahip karakterler için kullanılan tema yazı tipini alır veya ayarlar.`Font` nesne. |
| [TintAndShade](../../aspose.words/font/tintandshade/) { get; set; } | Bir rengi açan veya koyulaştıran bir double değeri alır veya ayarlar. |
| [Underline](../../aspose.words/font/underline/) { get; set; } | Yazı tipine uygulanan alt çizginin türünü alır veya ayarlar. |
| [UnderlineColor](../../aspose.words/font/underlinecolor/) { get; set; } | Yazı tipine uygulanan alt çizginin rengini alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [ClearFormatting](../../aspose.words/font/clearformatting/)() | Varsayılan yazı tipi biçimlendirmesine sıfırlar. |
| [HasDmlEffect](../../aspose.words/font/hasdmleffect/)(*[TextDmlEffect](../textdmleffect/)*) | Belirli DrawingML metin efektinin uygulanıp uygulanmadığını kontrol eder. |

## Notlar

Örnekleri oluşturmazsınız`Font` doğrudan sınıf. Sadece kullanın`Font` çeşitli nesnelerin yazı tipi özelliklerine erişmek için[`Run`](../run/) , [`Paragraph`](../paragraph/) ,[`Style`](../style/) ,[`DocumentBuilder`](../documentbuilder/).

## Örnekler

Bir metin dizisinin font özelliğini kullanarak nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

Bir belgeye kenarlıkla çevrili bir dizenin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

Liste biçimlendirmesiyle bir paragraf stilinin nasıl oluşturulacağını ve kullanılacağını gösterir.

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

// Belge oluşturucunun stilini liste biçimlendirmesi olmayan bir stile değiştirin ve başka bir paragraf yazın.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
