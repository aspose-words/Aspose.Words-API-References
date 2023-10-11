---
title: Class DocumentBuilder
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.DocumentBuilder sınıf. Metin resim ve diğer içerik ekleme yazı tipi paragraf ve bölüm formatını belirtme yöntemleri sağlar.
type: docs
weight: 450
url: /tr/net/aspose.words/documentbuilder/
---
## DocumentBuilder class

Metin, resim ve diğer içerik ekleme, yazı tipi, paragraf ve bölüm formatını belirtme yöntemleri sağlar.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Belge Oluşturucuya Genel Bakış](https://docs.aspose.com/words/net/document-builder-overview/) dokümantasyon makalesi.

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
| [CellFormat](../../aspose.words/documentbuilder/cellformat/) { get; } | Geçerli tablo hücresi biçimlendirme özelliklerini temsil eden bir nesneyi döndürür. |
| [CurrentNode](../../aspose.words/documentbuilder/currentnode/) { get; } | Bu DocumentBuilder'da seçili olan düğümü alır. |
| [CurrentParagraph](../../aspose.words/documentbuilder/currentparagraph/) { get; } | Bu bölümde o anda seçili olan paragrafı döndürür`DocumentBuilder` . |
| [CurrentSection](../../aspose.words/documentbuilder/currentsection/) { get; } | Bu bölümde o anda seçili olan bölümü döndürür`DocumentBuilder` . |
| [CurrentStory](../../aspose.words/documentbuilder/currentstory/) { get; } | Bu bölümde o anda seçili olan hikayeyi getirir`DocumentBuilder` . |
| [CurrentStructuredDocumentTag](../../aspose.words/documentbuilder/currentstructureddocumenttag/) { get; } | Şu anda seçili olan yapılandırılmış belge etiketini alır.`DocumentBuilder` . |
| [Document](../../aspose.words/documentbuilder/document/) { get; set; } | Alır veya ayarlar[`Document`](./document/)bu nesnenin eklendiği nesne. |
| [Font](../../aspose.words/documentbuilder/font/) { get; } | Geçerli yazı tipi biçimlendirme özelliklerini temsil eden bir nesneyi döndürür. |
| [IsAtEndOfParagraph](../../aspose.words/documentbuilder/isatendofparagraph/) { get; } | İadeler`doğru` İmleç geçerli paragrafın sonundaysa. |
| [IsAtEndOfStructuredDocumentTag](../../aspose.words/documentbuilder/isatendofstructureddocumenttag/) { get; } | İadeler **doğru** imleç yapılandırılmış bir belge etiketinin sonundaysa. |
| [IsAtStartOfParagraph](../../aspose.words/documentbuilder/isatstartofparagraph/) { get; } | İadeler`doğru` imleç geçerli paragrafın başındaysa (imleçten önce metin yok). |
| [Italic](../../aspose.words/documentbuilder/italic/) { get; set; } | Yazı tipi italik olarak biçimlendirilmişse doğrudur. |
| [ListFormat](../../aspose.words/documentbuilder/listformat/) { get; } | Geçerli liste biçimlendirme özelliklerini temsil eden bir nesneyi döndürür. |
| [PageSetup](../../aspose.words/documentbuilder/pagesetup/) { get; } | Geçerli sayfa düzenini ve bölüm özelliklerini temsil eden bir nesneyi döndürür. |
| [ParagraphFormat](../../aspose.words/documentbuilder/paragraphformat/) { get; } | Geçerli paragraf biçimlendirme özelliklerini temsil eden bir nesneyi döndürür. |
| [RowFormat](../../aspose.words/documentbuilder/rowformat/) { get; } | Geçerli tablo satırı biçimlendirme özelliklerini temsil eden bir nesneyi döndürür. |
| [Underline](../../aspose.words/documentbuilder/underline/) { get; set; } | Geçerli yazı tipinin alt çizgi türünü alır/ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [DeleteRow](../../aspose.words/documentbuilder/deleterow/)(int, int) | Tablodan bir satırı siler. |
| [EndBookmark](../../aspose.words/documentbuilder/endbookmark/)(string) | Belgedeki geçerli konumu yer imi sonu olarak işaretler. |
| [EndColumnBookmark](../../aspose.words/documentbuilder/endcolumnbookmark/)(string) | Belgedeki geçerli konumu sütun yer işareti sonu olarak işaretler. Konum bir tablo hücresinde olmalıdır. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange)() | Belgedeki geçerli konumu düzenlenebilir aralık sonu olarak işaretler. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange_1)(EditableRangeStart) | Belgedeki geçerli konumu düzenlenebilir aralık sonu olarak işaretler. |
| [EndRow](../../aspose.words/documentbuilder/endrow/)() | Belgedeki bir tablo satırını sonlandırır. |
| [EndTable](../../aspose.words/documentbuilder/endtable/)() | Belgedeki bir tabloyu sonlandırır. |
| [InsertBreak](../../aspose.words/documentbuilder/insertbreak/)(BreakType) | Belirtilen türde bir sonu belgeye ekler. |
| [InsertCell](../../aspose.words/documentbuilder/insertcell/)() | Belgeye bir tablo hücresi ekler. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_1)(ChartType, double, double) | Belgeye bir grafik nesnesi ekler ve bunu belirtilen boyuta ölçeklendirir. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart)(ChartType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Belgeye bir grafik nesnesi ekler ve bunu belirtilen boyuta ölçeklendirir. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox_1)(string, bool, int) | Geçerli konuma bir onay kutusu form alanı ekler. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox)(string, bool, bool, int) | Geçerli konuma bir onay kutusu form alanı ekler. |
| [InsertComboBox](../../aspose.words/documentbuilder/insertcombobox/)(string, string[], int) | Geçerli konuma bir birleşik giriş kutusu form alanı ekler. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument)(Document, ImportFormatMode) | İmleç konumuna bir belge ekler. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument_1)(Document, ImportFormatMode, ImportFormatOptions) | İmleç konumuna bir belge ekler. |
| [InsertDocumentInline](../../aspose.words/documentbuilder/insertdocumentinline/)(Document, ImportFormatMode, ImportFormatOptions) |  |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_1)(string) | Belgeye bir Word alanı ekler ve alan sonucunu günceller. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield)(FieldType, bool) | Belgeye bir Word alanı ekler ve isteğe bağlı olarak alan sonucunu günceller. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_2)(string, string) | Alan sonucunu güncellemeden belgeye bir Word alanı ekler. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote)(FootnoteType, string) | Belgeye dipnot veya son not ekler. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote_1)(FootnoteType, string, string) | Belgeye dipnot veya son not ekler. |
| [InsertHorizontalRule](../../aspose.words/documentbuilder/inserthorizontalrule/)() | Belgeye yatay bir kural şekli ekler. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml)(string) | Belgeye bir HTML dizesi ekler. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_2)(string, bool) | Belgeye bir HTML dizesi ekler. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_1)(string, HtmlInsertOptions) | Belgeye bir HTML dizesi ekler. Ek seçeneklerin belirtilmesine izin verir. |
| [InsertHyperlink](../../aspose.words/documentbuilder/inserthyperlink/)(string, string, bool) | Belgeye bir köprü ekler. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage)(byte[]) | Bayt dizisinden belgeye bir görüntü ekler. Resim satır içi ve %100 ölçekte eklenir. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_3)(Image) | .NET'ten bir görüntü eklerImage nesnesini belgeye ekleyin. Resim satır içi ve %100 ölçekte eklenir. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_6)(Stream) | Bir akıştan belgeye bir görüntü ekler. Resim satır içi ve %100 ölçekte eklenir. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_9)(string) | Bir dosyadan veya URL'den belgeye bir resim ekler. Resim satır içi ve %100 ölçekte eklenir. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_2)(byte[], double, double) | Bayt dizisinden satır içi bir görüntüyü belgeye ekler ve bunu belirtilen boyuta ölçeklendirir. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_5)(Image, double, double) | .NET'ten satır içi görüntü eklerImage nesnesini belgeye ekler ve onu belirtilen boyuta ölçeklendirir. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_8)(Stream, double, double) | Bir akıştan belgeye satır içi bir görüntü ekler ve bunu belirtilen boyuta ölçeklendirir. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_11)(string, double, double) | Bir dosyadan veya URL'den belgeye satır içi bir resim ekler ve bunu belirtilen boyuta ölçeklendirir. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_1)(byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Belirtilen konum ve boyutta bir bayt dizisinden bir görüntü ekler. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_4)(Image, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | .NET'ten bir görüntü eklerImage belirtilen konum ve boyuttaki nesne. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_7)(Stream, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Belirtilen konum ve boyutta bir akıştan bir görüntü ekler. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_10)(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Bir dosyadan veya URL'den belirtilen konuma ve boyuta bir resim ekler. |
| [InsertNode](../../aspose.words/documentbuilder/insertnode/)(Node) | İmlecin önüne bir düğüm ekler. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject)(Stream, string, bool, Stream) | Bir akıştan katıştırılmış bir OLE nesnesini belgeye ekler. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_1)(string, bool, bool, Stream) | Katıştırılmış veya bağlantılı bir OLE nesnesini bir dosyadan belgeye ekler. Dosya uzantısını kullanarak OLE nesne türünü algılar. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_2)(string, string, bool, bool, Stream) | Katıştırılmış veya bağlantılı bir OLE nesnesini bir dosyadan belgeye ekler. Verilen progID parametresini kullanarak OLE nesne türünü algılar. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon)(Stream, string, string, string) | Bir akıştan belgeye simge olarak gömülü bir OLE nesnesi ekler. Simge dosyasını ve resim yazısını belirtmeye izin verir. Verilen progID parametresini kullanarak OLE nesne türünü algılar. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_1)(string, bool, string, string) | Gömülü veya bağlantılı bir OLE nesnesini simge olarak belgeye ekler. Simge dosyasını ve resim yazısını belirtmeye izin verir. Dosya uzantısını kullanarak OLE nesne türünü algılar. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_2)(string, string, bool, string, string) | Gömülü veya bağlantılı bir OLE nesnesini simge olarak belgeye ekler. Simge dosyasını ve resim yazısını belirtmeye izin verir. Verilen progID parametresini kullanarak OLE nesne türünü algılar. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_1)(string, double, double) | Belgeye bir çevrimiçi video nesnesi ekler ve bunu belirtilen boyuta ölçeklendirir. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_3)(string, string, byte[], double, double) | Belgeye bir çevrimiçi video nesnesi ekler ve bunu belirtilen boyuta ölçeklendirir. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo)(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Belgeye bir çevrimiçi video nesnesi ekler ve bunu belirtilen boyuta ölçeklendirir. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_2)(string, string, byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Belgeye bir çevrimiçi video nesnesi ekler ve bunu belirtilen boyuta ölçeklendirir. |
| [InsertParagraph](../../aspose.words/documentbuilder/insertparagraph/)() | Belgeye paragraf sonu ekler. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape_1)(ShapeType, double, double) | Belirtilen tür ve boyutta satır içi şekil ekler. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape)(ShapeType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Belirtilen konuma, boyuta ve metin sarma türüne sahip serbest kayan şekil ekler. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline)(SignatureLineOptions) | Geçerli konuma bir imza satırı ekler. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline_1)(SignatureLineOptions, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, WrapType) | Belirtilen konuma bir imza satırı ekler. |
| [InsertStyleSeparator](../../aspose.words/documentbuilder/insertstyleseparator/)() | Belgeye stil ayırıcıyı ekler. |
| [InsertTableOfContents](../../aspose.words/documentbuilder/inserttableofcontents/)(string) | Belgeye bir TOC (içindekiler tablosu) alanı ekler. |
| [InsertTextInput](../../aspose.words/documentbuilder/inserttextinput/)(string, TextFormFieldType, string, string, int) | Geçerli konuma bir metin formu alanı ekler. |
| [MoveTo](../../aspose.words/documentbuilder/moveto/)(Node) | İmleci satır içi düğüme veya paragrafın sonuna taşır. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark)(string) | İmleci bir yer imine taşır. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark_1)(string, bool, bool) | İmleci daha büyük bir hassasiyetle yer imine taşır. |
| [MoveToCell](../../aspose.words/documentbuilder/movetocell/)(int, int, int, int) | İmleci geçerli bölümdeki bir tablo hücresine taşır. |
| [MoveToDocumentEnd](../../aspose.words/documentbuilder/movetodocumentend/)() | İmleci belgenin sonuna taşır. |
| [MoveToDocumentStart](../../aspose.words/documentbuilder/movetodocumentstart/)() | İmleci belgenin başına taşır. |
| [MoveToField](../../aspose.words/documentbuilder/movetofield/)(Field, bool) | İmleci belgedeki bir alana taşır. |
| [MoveToHeaderFooter](../../aspose.words/documentbuilder/movetoheaderfooter/)(HeaderFooterType) | İmleci geçerli bölümdeki üstbilgi veya altbilginin başlangıcına taşır. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield)(string) | İmleci belirtilen birleştirme alanının hemen ötesindeki bir konuma taşır ve birleştirme alanını kaldırır. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield_1)(string, bool, bool) | Birleştirme alanını belirtilen birleştirme alanına taşır. |
| [MoveToParagraph](../../aspose.words/documentbuilder/movetoparagraph/)(int, int) | İmleci geçerli bölümdeki bir paragrafa taşır. |
| [MoveToSection](../../aspose.words/documentbuilder/movetosection/)(int) | İmleci belirtilen bölümdeki gövdenin başlangıcına taşır. |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag_1)(int, int) | İmleci geçerli bölümdeki yapılandırılmış belge etiketine taşır. |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag)(StructuredDocumentTag, int) | İmleci yapılandırılmış belge etiketine taşır. |
| [PopFont](../../aspose.words/documentbuilder/popfont/)() | Daha önce yığına kaydedilen karakter formatını alır. |
| [PushFont](../../aspose.words/documentbuilder/pushfont/)() | Geçerli karakter formatını yığına kaydeder. |
| [StartBookmark](../../aspose.words/documentbuilder/startbookmark/)(string) | Belgedeki geçerli konumu yer imi başlangıcı olarak işaretler. |
| [StartColumnBookmark](../../aspose.words/documentbuilder/startcolumnbookmark/)(string) | Belgedeki geçerli konumu sütun yer işareti başlangıcı olarak işaretler. Konum bir tablo hücresinde olmalıdır. |
| [StartEditableRange](../../aspose.words/documentbuilder/starteditablerange/)() | Düzenlenebilir aralık başlangıcı olarak belgedeki geçerli konumu işaretler. |
| [StartTable](../../aspose.words/documentbuilder/starttable/)() | Belgede bir tablo başlatır. |
| [Write](../../aspose.words/documentbuilder/write/)(string) | Belgeye geçerli ekleme konumunda bir dize ekler. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln)() | Belgeye paragraf sonu ekler. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln_1)(string) | Belgeye bir dize ve paragraf sonu ekler. |

### Notlar

`DocumentBuilder` bir inşa etme sürecini gerçekleştirir[`Document`](../document/) daha kolay. [`Document`](../document/) bir düğüm ağacından oluşan bileşik bir nesnedir ve content düğümlerini doğrudan ağaca eklemek mümkün olsa da, ağaç yapısının iyi anlaşılmasını gerektirir. `DocumentBuilder` karmaşık yapısının bir “cephesi”dir.[`Document`](../document/) ve Allow 'nin içerik ve biçimlendirmeyi hızlı ve kolay bir şekilde eklemesine izin verir.

Oluşturmak`DocumentBuilder` ve bunu bir şeyle ilişkilendirin[`Document`](../document/).

`DocumentBuilder` aradığınızda metnin ekleneceği dahili bir imleç var [`Write`](./write/) ,[`Writeln`](./writeln/) ,[`InsertBreak`](./insertbreak/) ve diğer yöntemler. Gezinebilirsiniz`DocumentBuilder` Çeşitli MoveToXXX yöntemlerini kullanarak imleci belgede farklı bir konuma getirin.

Kullan[`Font`](./font/)belgedeki geçerli konumdan itibaren eklenen tüm metinlere uygulanacak karakter biçimlendirmesini belirtme özelliği.

Kullan[`ParagraphFormat`](./paragraphformat/) current ve eklenecek tüm paragraflar için paragraf biçimlendirmesini belirtme özelliği.

Kullan[`PageSetup`](./pagesetup/) current bölümü ve eklenecek tüm bölümler için sayfa ve bölüm özelliklerini belirtme özelliği.

Kullan[`CellFormat`](./cellformat/) Ve[`RowFormat`](./rowformat/) tablo hücreleri ve satırlar için biçimlendirme özelliklerini belirtmek için özellikler. Kullanıcı[`InsertCell`](./insertcell/) ve [`EndRow`](./endrow/) tablo oluşturma yöntemleri.

Dikkat[`Font`](./font/) ,[`ParagraphFormat`](./paragraphformat/) Ve[`PageSetup`](./pagesetup/) yeni konumda mevcut olan biçimlendirme özelliklerini yansıtmak için belgede farklı bir yere gittiğinizde özellikler güncellenir.

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

DocumentBuilder'ı kullanarak bir belgede üstbilgilerin ve altbilgilerin nasıl oluşturulacağını gösterir.

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

Özel kenarlıklara sahip bir tablonun nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Belge oluşturucu için tablo biçimlendirme seçeneklerini ayarlama
// bunları eklediğimiz her satıra ve hücreye uygulayacaktır.
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

// Biçimlendirmeyi değiştirmek onu geçerli hücreye uygulayacaktır,
// ve daha sonra oluşturucuyla oluşturduğumuz yeni hücreler.
// Bu daha önce eklediğimiz hücreleri etkilemeyecektir.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Dikey metne sığacak şekilde satır yüksekliğini artırın.
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


