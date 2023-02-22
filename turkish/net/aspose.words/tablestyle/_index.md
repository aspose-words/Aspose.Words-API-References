---
title: Class TableStyle
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.TableStyle sınıf. Bir tablo stilini temsil eder.
type: docs
weight: 5920
url: /tr/net/aspose.words/tablestyle/
---
## TableStyle class

Bir tablo stilini temsil eder.

```csharp
public class TableStyle : Style
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Aliases](../../aspose.words/style/aliases/) { get; } | Bu stilin tüm diğer adlarını alır. Stilin takma adı yoksa, boş dize dizisi döndürülür. |
| [Alignment](../../aspose.words/tablestyle/alignment/) { get; set; } | Tablo stili için hizalamayı belirtir. |
| [AllowBreakAcrossPages](../../aspose.words/tablestyle/allowbreakacrosspages/) { get; set; } | Tablo satırındaki metnin sayfa sonu boyunca bölünmesine izin verilip verilmediğini belirten bir bayrak alır veya ayarlar. |
| [BaseStyleName](../../aspose.words/style/basestylename/) { get; set; } | Bu stilin dayandığı stilin adını alır/ayarlar. |
| [Bidi](../../aspose.words/tablestyle/bidi/) { get; set; } | Bunun sağdan sola tablo için bir stil olup olmadığını alır veya ayarlar. |
| [Borders](../../aspose.words/tablestyle/borders/) { get; } | Stil için varsayılan hücre kenarlıkları koleksiyonunu alır. |
| [BottomPadding](../../aspose.words/tablestyle/bottompadding/) { get; set; } | Tablo hücrelerinin içeriğinin altına eklenecek boşluk miktarını (puan olarak) alır veya ayarlar. |
| [BuiltIn](../../aspose.words/style/builtin/) { get; } | Bu stil MS Word'deki yerleşik stillerden biriyse doğrudur. |
| [CellSpacing](../../aspose.words/tablestyle/cellspacing/) { get; set; } | Hücreler arasındaki boşluk miktarını (nokta olarak) alır veya ayarlar. |
| [ColumnStripe](../../aspose.words/tablestyle/columnstripe/) { get; set; } | Stil tek/çift sütun bantlamasını belirttiğinde, bantlamaya dahil edilecek sütun sayısını alır veya ayarlar. |
| [ConditionalStyles](../../aspose.words/tablestyle/conditionalstyles/) { get; } | Bu tablo stili için tanımlanabilecek koşullu stiller koleksiyonu. |
| [Document](../../aspose.words/style/document/) { get; } | Sahip belgesini alır. |
| [Font](../../aspose.words/style/font/) { get; } | Stilin karakter biçimlendirmesini alır. |
| [IsHeading](../../aspose.words/style/isheading/) { get; } | Stil, yerleşik Başlık stillerinden biri olduğunda doğrudur. |
| [IsQuickStyle](../../aspose.words/style/isquickstyle/) { get; set; } | Bu stilin MS Word UI içindeki Hızlı Stil galerisinde gösterilip gösterilmeyeceğini belirtir. |
| [LeftIndent](../../aspose.words/tablestyle/leftindent/) { get; set; } | Bir tablonun sol girintisini temsil eden değeri alır veya ayarlar. |
| [LeftPadding](../../aspose.words/tablestyle/leftpadding/) { get; set; } | Tablo hücrelerinin içeriğinin soluna eklenecek boşluk miktarını (puan olarak) alır veya ayarlar. |
| [LinkedStyleName](../../aspose.words/style/linkedstylename/) { get; } | Buna bağlı Stilin adını alır. Hiçbir stil bağlı değilse Boş dize döndürür. |
| [List](../../aspose.words/style/list/) { get; } | Bu liste stilinin biçimlendirmesini tanımlayan listeyi alır. |
| [ListFormat](../../aspose.words/style/listformat/) { get; } | Paragraf stilinin liste biçimlendirme özelliklerine erişim sağlar. |
| [Name](../../aspose.words/style/name/) { get; set; } | Stilin adını alır veya ayarlar. |
| [NextParagraphStyleName](../../aspose.words/style/nextparagraphstylename/) { get; set; } | Belirtilen stille biçimlendirilmiş a paragrafından sonra eklenen yeni paragrafa otomatik olarak uygulanacak stilin adını alır/ayarlar. |
| [ParagraphFormat](../../aspose.words/style/paragraphformat/) { get; } | Stilin paragraf biçimlendirmesini alır. |
| [RightPadding](../../aspose.words/tablestyle/rightpadding/) { get; set; } | Tablo hücrelerinin içeriğinin sağına eklenecek boşluk miktarını (puan olarak) alır veya ayarlar. |
| [RowStripe](../../aspose.words/tablestyle/rowstripe/) { get; set; } | Stil tek/çift satır bantlamasını belirttiğinde bantlamaya dahil edilecek satır sayısını alır veya ayarlar. |
| [Shading](../../aspose.words/tablestyle/shading/) { get; } | [`Shading`](../shading/) tablo hücreleri için gölgeleme biçimlendirmesine başvuran nesne. |
| [StyleIdentifier](../../aspose.words/style/styleidentifier/) { get; } | Yerleşik bir stil için yerel ayardan bağımsız stil tanımlayıcısını alır. |
| [Styles](../../aspose.words/style/styles/) { get; } | Bu stilin ait olduğu stiller koleksiyonunu alır. |
| [TopPadding](../../aspose.words/tablestyle/toppadding/) { get; set; } | Tablo hücrelerinin içeriğinin üzerine eklenecek boşluk miktarını (puan olarak) alır veya ayarlar. |
| [Type](../../aspose.words/style/type/) { get; } | Stil türünü (paragraf veya karakter) alır. |
| [VerticalAlignment](../../aspose.words/tablestyle/verticalalignment/) { get; set; } | Hücreler için dikey hizalamayı belirtir. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Equals](../../aspose.words/style/equals/)(Style) | Belirtilen stille karşılaştırır. Stiller İstd'ler yalnızca yerleşik stiller için karşılaştırılır. Stil varsayılanları karşılaştırmaya dahil edilmez. Temel stil, bağlantılı stil ve sonraki paragraf stili yinelemeli olarak karşılaştırılır. |
| [Remove](../../aspose.words/style/remove/)() | Belirtilen stili belgeden kaldırır. |

### Örnekler

Tablo için özel stil ayarlarının nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Name");
builder.InsertCell();
builder.Write("مرحبًا");
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.AllowBreakAcrossPages = true;
tableStyle.Bidi = true;
tableStyle.CellSpacing = 5;
tableStyle.BottomPadding = 20;
tableStyle.LeftPadding = 5;
tableStyle.RightPadding = 10;
tableStyle.TopPadding = 20;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;
tableStyle.VerticalAlignment = CellVerticalAlignment.Center;

table.Style = tableStyle;

// Bir tablonun stil özelliklerini ayarlamak, tablonun özelliklerini etkileyebilir.
Assert.True(table.Bidi);
Assert.AreEqual(5.0d, table.CellSpacing);
Assert.AreEqual("MyTableStyle1", table.StyleName);

doc.Save(ArtifactsDir + "Table.TableStyleCreation.docx");
```

### Ayrıca bakınız

* class [Style](../style/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


