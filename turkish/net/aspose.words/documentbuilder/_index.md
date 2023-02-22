---
title: Class DocumentBuilder
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.DocumentBuilder sınıf. Metin resim ve diğer içeriği eklemek yazı tipini paragrafı ve bölüm biçimlendirmesini belirtmek için yöntemler sağlar.
type: docs
weight: 440
url: /tr/net/aspose.words/documentbuilder/
---
## DocumentBuilder class

Metin, resim ve diğer içeriği eklemek, yazı tipini, paragrafı ve bölüm biçimlendirmesini belirtmek için yöntemler sağlar.

```csharp
public class DocumentBuilder
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [DocumentBuilder](documentbuilder/#constructor)() | Bu sınıfın yeni bir örneğini başlatır. |
| [DocumentBuilder](documentbuilder/#constructor_1)(Document) | Bu sınıfın yeni bir örneğini başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Bold](../../aspose.words/documentbuilder/bold/) { get; set; } | Yazı tipi kalın olarak biçimlendirilmişse doğrudur. |
| [CellFormat](../../aspose.words/documentbuilder/cellformat/) { get; } | Geçerli tablo hücresi biçimlendirme özelliklerini temsil eden bir nesne döndürür. |
| [CurrentNode](../../aspose.words/documentbuilder/currentnode/) { get; } | Bu DocumentBuilder'da seçili olan düğümü alır. |
| [CurrentParagraph](../../aspose.words/documentbuilder/currentparagraph/) { get; } | Bu DocumentBuilder'da seçili olan paragrafı alır. |
| [CurrentSection](../../aspose.words/documentbuilder/currentsection/) { get; } | Bu DocumentBuilder'da seçili olan bölümü alır. |
| [CurrentStory](../../aspose.words/documentbuilder/currentstory/) { get; } | Bu DocumentBuilder'da seçili olan öyküyü alır. |
| [Document](../../aspose.words/documentbuilder/document/) { get; set; } | Alır veya ayarlar[`Document`](./document/) bu nesnenin eklendiği nesne. |
| [Font](../../aspose.words/documentbuilder/font/) { get; } | Geçerli yazı tipi biçimlendirme özelliklerini temsil eden bir nesne döndürür. |
| [IsAtEndOfParagraph](../../aspose.words/documentbuilder/isatendofparagraph/) { get; } | İmleç geçerli paragrafın sonundaysa true değerini döndürür. |
| [IsAtStartOfParagraph](../../aspose.words/documentbuilder/isatstartofparagraph/) { get; } | İmleç geçerli paragrafın başındaysa doğru döndürür (imleçten önce metin yok). |
| [Italic](../../aspose.words/documentbuilder/italic/) { get; set; } | Yazı tipi italik olarak biçimlendirilmişse doğrudur. |
| [ListFormat](../../aspose.words/documentbuilder/listformat/) { get; } | Geçerli liste biçimlendirme özelliklerini temsil eden bir nesne döndürür. |
| [PageSetup](../../aspose.words/documentbuilder/pagesetup/) { get; } | Geçerli sayfa düzenini ve bölüm özelliklerini temsil eden bir nesne döndürür. |
| [ParagraphFormat](../../aspose.words/documentbuilder/paragraphformat/) { get; } | Geçerli paragraf biçimlendirme özelliklerini temsil eden bir nesne döndürür. |
| [RowFormat](../../aspose.words/documentbuilder/rowformat/) { get; } | Geçerli tablo satırı biçimlendirme özelliklerini temsil eden bir nesne döndürür. |
| [Underline](../../aspose.words/documentbuilder/underline/) { get; set; } | Geçerli yazı tipi için alt çizgi türünü alır/ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [DeleteRow](../../aspose.words/documentbuilder/deleterow/)(int, int) | Tablodan bir satırı siler. |
| [EndBookmark](../../aspose.words/documentbuilder/endbookmark/)(string) | Belgedeki geçerli konumu yer imi sonu olarak işaretler. |
| [EndColumnBookmark](../../aspose.words/documentbuilder/endcolumnbookmark/)(string) | Belgedeki geçerli konumu bir sütun yer imi sonu olarak işaretler. Konum bir tablo hücresinde olmalıdır. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange)() | Belgedeki geçerli konumu düzenlenebilir bir aralık sonu olarak işaretler. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange_1)(EditableRangeStart) | Belgedeki geçerli konumu düzenlenebilir bir aralık sonu olarak işaretler. |
| [EndRow](../../aspose.words/documentbuilder/endrow/)() | Belgedeki bir tablo satırını sonlandırır. |
| [EndTable](../../aspose.words/documentbuilder/endtable/)() | Belgedeki bir tabloyu sonlandırır. |
| [InsertBreak](../../aspose.words/documentbuilder/insertbreak/)(BreakType) | Belgeye belirtilen türde bir kesme ekler. |
| [InsertCell](../../aspose.words/documentbuilder/insertcell/)() | Belgeye bir tablo hücresi ekler. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_1)(ChartType, double, double) | Belgeye bir grafik nesnesi ekler ve onu belirtilen boyuta ölçeklendirir. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart)(ChartType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Belgeye bir grafik nesnesi ekler ve onu belirtilen boyuta ölçeklendirir. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox_1)(string, bool, int) | Geçerli konuma bir onay kutusu form alanı ekler. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox)(string, bool, bool, int) | Geçerli konuma bir onay kutusu form alanı ekler. |
| [InsertComboBox](../../aspose.words/documentbuilder/insertcombobox/)(string, string[], int) | Geçerli konuma bir birleşik giriş formu alanı ekler. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument)(Document, ImportFormatMode) | İmleç konumuna bir belge ekler. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument_1)(Document, ImportFormatMode, ImportFormatOptions) | İmleç konumuna bir belge ekler. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_1)(string) | Belgeye bir Word alanı ekler ve alan sonucunu günceller. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield)(FieldType, bool) | Belgeye bir Word alanı ekler ve isteğe bağlı olarak alan sonucunu günceller. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_2)(string, string) | Alan sonucunu güncellemeden belgeye bir Word alanı ekler. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote)(FootnoteType, string) | Belgeye bir dipnot veya son not ekler. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote_1)(FootnoteType, string, string) | Belgeye bir dipnot veya son not ekler. |
| [InsertHorizontalRule](../../aspose.words/documentbuilder/inserthorizontalrule/)() | Belgeye yatay bir kural şekli ekler. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml)(string) | Belgeye bir HTML dizesi ekler. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_2)(string, bool) | Belgeye bir HTML dizesi ekler. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_1)(string, HtmlInsertOptions) | Belgeye bir HTML dizesi ekler. Ek seçenekleri belirlemeye izin verir. |
| [InsertHyperlink](../../aspose.words/documentbuilder/inserthyperlink/)(string, string, bool) | Belgeye bir köprü ekler. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage)(byte[]) | Belgeye bir bayt dizisinden bir görüntü ekler. Resim satır içi ve %100 ölçekte eklenir. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_3)(Image) | Bir .NET'ten bir görüntü eklerImage nesnesini belgeye yerleştirin. Resim satır içi ve %100 ölçekte eklenir. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_6)(Stream) | Bir akıştan belgeye bir görüntü ekler. Resim satır içi ve %100 ölçekte eklenir. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_9)(string) | Bir dosyadan veya URL'den belgeye bir resim ekler. Resim satır içi ve %100 ölçekte eklenir. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_2)(byte[], double, double) | Belgeye bir bayt dizisinden satır içi bir görüntü ekler ve onu belirtilen boyuta ölçekler. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_5)(Image, double, double) | Bir .NET'ten satır içi görüntü eklerImage nesneyi belgeye ekler ve onu belirtilen boyuta ölçeklendirir. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_8)(Stream, double, double) | Bir akıştan belgeye satır içi bir görüntü ekler ve onu belirtilen boyuta ölçeklendirir. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_11)(string, double, double) | Bir dosyadan veya URL'den belgeye satır içi bir resim ekler ve onu belirtilen boyuta ölçeklendirir. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_1)(byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Belirtilen konum ve boyutta bir bayt dizisinden bir görüntü ekler. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_4)(Image, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Bir .NET'ten bir görüntü eklerImage belirtilen konum ve boyutta nesne. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_7)(Stream, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Belirtilen konum ve boyutta bir akıştan bir görüntü ekler. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_10)(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Belirtilen konum ve boyutta bir dosyadan veya URL'den bir resim ekler. |
| [InsertNode](../../aspose.words/documentbuilder/insertnode/)(Node) | Geçerli paragrafın içine imlecin önüne bir metin düzeyi düğümü ekler. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject)(Stream, string, bool, Stream) | Bir akıştan belgeye katıştırılmış bir OLE nesnesi ekler. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_1)(string, bool, bool, Stream) | Bir dosyadan belgeye katıştırılmış veya bağlantılı bir OLE nesnesi ekler. Dosya uzantısını kullanarak OLE nesne türünü algılar. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_2)(string, string, bool, bool, Stream) | Bir dosyadan belgeye katıştırılmış veya bağlantılı bir OLE nesnesi ekler. Verilen progID parametresini kullanarak OLE nesne türünü algılar. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon)(Stream, string, string, string) | Belgeye bir akıştan simge olarak katıştırılmış bir OLE nesnesi ekler. Simge dosyası ve resim yazısı belirtmeye izin verir. Verilen progID parametresini kullanarak OLE nesne türünü algılar. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_1)(string, bool, string, string) | Belgeye simge olarak katıştırılmış veya bağlantılı bir OLE nesnesi ekler. Simge dosyası ve resim yazısı belirtmenize izin verir. Dosya uzantısını kullanarak OLE nesne türünü algılar. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_2)(string, string, bool, string, string) | Belgeye simge olarak katıştırılmış veya bağlantılı bir OLE nesnesi ekler. Simge dosyası ve resim yazısı belirtmenize izin verir. Verilen progID parametresini kullanarak OLE nesne türünü algılar. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_1)(string, double, double) | Belgeye çevrimiçi bir video nesnesi ekler ve onu belirtilen boyuta ölçeklendirir. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_3)(string, string, byte[], double, double) | Belgeye çevrimiçi bir video nesnesi ekler ve onu belirtilen boyuta ölçeklendirir. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo)(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Belgeye çevrimiçi bir video nesnesi ekler ve onu belirtilen boyuta ölçeklendirir. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_2)(string, string, byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Belgeye çevrimiçi bir video nesnesi ekler ve onu belirtilen boyuta ölçeklendirir. |
| [InsertParagraph](../../aspose.words/documentbuilder/insertparagraph/)() | Belgeye bir paragraf sonu ekler. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape_1)(ShapeType, double, double) | Belirtilen tür ve boyutta satır içi şekil ekler. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape)(ShapeType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Belirtilen konum, boyut ve metin sarma türü ile serbest kayan şekil ekler. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline)(SignatureLineOptions) | Geçerli konuma bir imza satırı ekler. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline_1)(SignatureLineOptions, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, WrapType) | Belirtilen konuma bir imza satırı ekler. |
| [InsertStyleSeparator](../../aspose.words/documentbuilder/insertstyleseparator/)() | Belgeye stil ayırıcı ekler. |
| [InsertTableOfContents](../../aspose.words/documentbuilder/inserttableofcontents/)(string) | Belgeye bir İçindekiler (içindekiler) alanı ekler. |
| [InsertTextInput](../../aspose.words/documentbuilder/inserttextinput/)(string, TextFormFieldType, string, string, int) | Geçerli konuma bir metin formu alanı ekler. |
| [MoveTo](../../aspose.words/documentbuilder/moveto/)(Node) | İmleci satır içi bir düğüme veya paragrafın sonuna taşır. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark)(string) | İmleci bir yer işaretine taşır. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark_1)(string, bool, bool) | İmleci daha hassas bir şekilde bir yer işaretine taşır. |
| [MoveToCell](../../aspose.words/documentbuilder/movetocell/)(int, int, int, int) | İmleci geçerli bölümdeki bir tablo hücresine taşır. |
| [MoveToDocumentEnd](../../aspose.words/documentbuilder/movetodocumentend/)() | İmleci belgenin sonuna taşır. |
| [MoveToDocumentStart](../../aspose.words/documentbuilder/movetodocumentstart/)() | İmleci belgenin başına taşır. |
| [MoveToField](../../aspose.words/documentbuilder/movetofield/)(Field, bool) | İmleci belgedeki bir alana taşır. |
| [MoveToHeaderFooter](../../aspose.words/documentbuilder/movetoheaderfooter/)(HeaderFooterType) | İmleci, geçerli bölümdeki bir üstbilgi veya altbilginin başına taşır. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield)(string) | İmleci belirtilen birleştirme alanının hemen ötesinde bir konuma taşır ve birleştirme alanını kaldırır. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield_1)(string, bool, bool) | Birleştirme alanını belirtilen birleştirme alanına taşır. |
| [MoveToParagraph](../../aspose.words/documentbuilder/movetoparagraph/)(int, int) | İmleci geçerli bölümdeki bir paragrafa taşır. |
| [MoveToSection](../../aspose.words/documentbuilder/movetosection/)(int) | İmleci belirtilen bir bölümde gövdenin başına taşır. |
| [PopFont](../../aspose.words/documentbuilder/popfont/)() | Daha önce yığına kaydedilmiş karakter biçimlendirmesini alır. |
| [PushFont](../../aspose.words/documentbuilder/pushfont/)() | Geçerli karakter biçimlendirmesini yığına kaydeder. |
| [StartBookmark](../../aspose.words/documentbuilder/startbookmark/)(string) | Belgedeki geçerli konumu yer imi başlangıcı olarak işaretler. |
| [StartColumnBookmark](../../aspose.words/documentbuilder/startcolumnbookmark/)(string) | Belgedeki geçerli konumu bir sütun yer imi başlangıcı olarak işaretler. Konum bir tablo hücresinde olmalıdır. |
| [StartEditableRange](../../aspose.words/documentbuilder/starteditablerange/)() | Belgedeki geçerli konumu düzenlenebilir bir aralık başlangıcı olarak işaretler. |
| [StartTable](../../aspose.words/documentbuilder/starttable/)() | Belgede bir tablo başlatır. |
| [Write](../../aspose.words/documentbuilder/write/)(string) | Geçerli ekleme konumunda belgeye bir dize ekler. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln)() | Belgeye bir paragraf sonu ekler. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln_1)(string) | Belgeye bir dize ve paragraf sonu ekler. |

### Notlar

**Belge Oluşturucu** inşa etme sürecini yapar **Belge** daha kolay.  **Belge**bir düğüm ağacından oluşan bileşik bir nesnedir ve content düğümlerini doğrudan ağaca eklemek mümkündür, ancak ağaç yapısının iyi anlaşılmasını gerektirir.  **Belge Oluşturucu** karmaşık yapısı için bir "cephe"dir. **Belge** ve 'nin içerik ve biçimlendirmeyi hızlı ve kolay bir şekilde eklemesine izin verir.

Oluşturmak **Belge Oluşturucu** ve bir ile ilişkilendirin[`Document`](./document/).

bu **Belge Oluşturucu** aradığınızda metnin ekleneceği bir dahili imleç var [`Write`](./write/) ,[`Writeln`](./writeln/) ,[`InsertBreak`](./insertbreak/) ve diğer yöntemler. gezinebilirsiniz **Belge Oluşturucu** çeşitli MoveToXXX yöntemlerini kullanarak bir belgede imleci farklı bir konuma getirin.

Kullan[`Font`](./font/) belgedeki geçerli konumdan itibaren eklenen tüm metne uygulanacak karakter biçimlendirmesini belirtmek için özellik.

Kullan[`ParagraphFormat`](./paragraphformat/) current ve eklenecek tüm paragraflar için paragraf biçimlendirmesini belirtmek için özellik.

Kullan[`PageSetup`](./pagesetup/)current bölümü ve eklenecek tüm bölümler için sayfa ve bölüm özelliklerini belirtmek için özellik.

Kullan[`CellFormat`](./cellformat/) ve[`RowFormat`](./rowformat/) tablo hücreleri ve satırları için biçimlendirme özelliklerini belirtmek için özellikler . kullanıcı[`InsertCell`](./insertcell/) and [`EndRow`](./endrow/) tablo oluşturma yöntemleri.

Dikkat **Yazı tipi** , **Paragraf Biçimi** ve **Sayfa ayarı** özellikler, yeni konumda mevcut olan biçimlendirme özelliklerini yansıtmak için belgede farklı bir yere gittiğinizde güncellenir.

### Örnekler

Tablo oluşturmak için belge oluşturucunun nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Tabloyu başlatın, ardından ilk satırı iki hücreyle doldurun.
builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");

// Yeni bir satır başlatmak için oluşturucunun "EndRow" yöntemini çağırın.
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateTable.docx");
```

DocumentBuilder kullanılarak bir belgede nasıl üstbilgi ve altbilgi oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// İlk, çift ve tek sayfalar için farklı üstbilgi ve altbilgi istediğimizi belirtin.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Başlıkları oluşturun, ardından her başlık türünü görüntülemek için belgeye üç sayfa ekleyin.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

Özel kenarlıklı bir tablonun nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Bir belge oluşturucu için tablo biçimlendirme seçeneklerini ayarlama
// onları eklediğimiz her satıra ve hücreye uygulayacak.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;

builder.CellFormat.ClearFormatting();
builder.CellFormat.Width = 150;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.CellFormat.Shading.BackgroundPatternColor = Color.GreenYellow;
builder.CellFormat.WrapText = false;
builder.CellFormat.FitText = true;

builder.RowFormat.ClearFormatting();
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.RowFormat.Height = 50;
builder.RowFormat.Borders.LineStyle = LineStyle.Engrave3D;
builder.RowFormat.Borders.Color = Color.Orange;

builder.InsertCell();
builder.Write("Row 1, Col 1");

builder.InsertCell();
builder.Write("Row 1, Col 2");
builder.EndRow();

// Biçimlendirmeyi değiştirmek, onu geçerli hücreye uygular,
// ve daha sonra oluşturucu ile oluşturduğumuz yeni hücreler.
// Bu daha önce eklediğimiz hücreleri etkilemeyecektir.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Dikey metne sığdırmak için satır yüksekliğini artırın.
builder.InsertCell();
builder.RowFormat.Height = 150;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 3, Col 1");

builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 3, Col 2");

builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTable.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


