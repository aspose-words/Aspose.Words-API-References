---
title: DocumentBuilder Class
linktitle: DocumentBuilder
articleTitle: DocumentBuilder
second_title: .NET için Aspose.Words
description: Aspose.Words.DocumentBuilder sınıfını keşfedin; belgelerinize metin, resim ve biçimlendirme öğelerini zahmetsizce eklemek için çözümünüz.
type: docs
weight: 660
url: /tr/net/aspose.words/documentbuilder/
---
## DocumentBuilder class

Metin, resim ve diğer içerikleri eklemek, yazı tipini, paragrafı ve bölüm biçimlendirmesini belirtmek için yöntemler sağlar.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Belge Oluşturucu Genel Bakış](https://docs.aspose.com/words/net/document-builder-overview/) belgeleme makalesi.

```csharp
public class DocumentBuilder
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [DocumentBuilder](documentbuilder/#constructor)() | Bu sınıfın yeni bir örneğini başlatır. |
| [DocumentBuilder](documentbuilder/#constructor_1)(*[Document](../document/)*) | Bu sınıfın yeni bir örneğini başlatır. |
| [DocumentBuilder](documentbuilder/#constructor_3)(*[DocumentBuilderOptions](../documentbuilderoptions/)*) | Bu sınıfın yeni bir örneğini başlatır. |
| [DocumentBuilder](documentbuilder/#constructor_2)(*[Document](../document/), [DocumentBuilderOptions](../documentbuilderoptions/)*) | Bu sınıfın yeni bir örneğini başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Bold](../../aspose.words/documentbuilder/bold/) { get; set; } | Yazı tipi kalın olarak biçimlendirilmişse doğrudur. |
| [CellFormat](../../aspose.words/documentbuilder/cellformat/) { get; } | Geçerli tablo hücresi biçimlendirme özelliklerini temsil eden bir nesne döndürür. |
| [CurrentNode](../../aspose.words/documentbuilder/currentnode/) { get; } | Bu DocumentBuilder'da şu anda seçili olan düğümü alır. |
| [CurrentParagraph](../../aspose.words/documentbuilder/currentparagraph/) { get; } | Bu bölümde şu anda seçili olan paragrafı alır`DocumentBuilder` . |
| [CurrentSection](../../aspose.words/documentbuilder/currentsection/) { get; } | Bu bölümde şu anda seçili olan bölümü alır`DocumentBuilder` . |
| [CurrentStory](../../aspose.words/documentbuilder/currentstory/) { get; } | Bu bölümde şu anda seçili olan hikayeyi alır`DocumentBuilder` . |
| [CurrentStructuredDocumentTag](../../aspose.words/documentbuilder/currentstructureddocumenttag/) { get; } | Bu belgede şu anda seçili olan yapılandırılmış belge etiketini alır`DocumentBuilder` . |
| [Document](../../aspose.words/documentbuilder/document/) { get; set; } | Alır veya ayarlar[`Document`](./document/) bu nesnenin bağlı olduğu nesne. |
| [Font](../../aspose.words/documentbuilder/font/) { get; } | Geçerli yazı tipi biçimlendirme özelliklerini temsil eden bir nesne döndürür. |
| [IsAtEndOfParagraph](../../aspose.words/documentbuilder/isatendofparagraph/) { get; } | Geri Döndürür`doğru` imleç geçerli paragrafın sonunda ise. |
| [IsAtEndOfStructuredDocumentTag](../../aspose.words/documentbuilder/isatendofstructureddocumenttag/) { get; } | Geri Döndürür**doğru** imleç yapılandırılmış bir belge etiketinin sonundaysa. |
| [IsAtStartOfParagraph](../../aspose.words/documentbuilder/isatstartofparagraph/) { get; } | Geri Döndürür`doğru`imleç geçerli paragrafın başındaysa (imleçten önce metin yoksa). |
| [Italic](../../aspose.words/documentbuilder/italic/) { get; set; } | Yazı tipi italik olarak biçimlendirilmişse doğrudur. |
| [ListFormat](../../aspose.words/documentbuilder/listformat/) { get; } | Geçerli liste biçimlendirme özelliklerini temsil eden bir nesne döndürür. |
| [PageSetup](../../aspose.words/documentbuilder/pagesetup/) { get; } | Geçerli sayfa düzenini ve bölüm özelliklerini temsil eden bir nesne döndürür. |
| [ParagraphFormat](../../aspose.words/documentbuilder/paragraphformat/) { get; } | Geçerli paragraf biçimlendirme özelliklerini temsil eden bir nesne döndürür. |
| [RowFormat](../../aspose.words/documentbuilder/rowformat/) { get; } | Geçerli tablo satır biçimlendirme özelliklerini temsil eden bir nesne döndürür. |
| [Underline](../../aspose.words/documentbuilder/underline/) { get; set; } | Geçerli yazı tipi için alt çizgi türünü alır/ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [DeleteRow](../../aspose.words/documentbuilder/deleterow/)(*int, int*) | Bir tablodan bir satırı siler. |
| [EndBookmark](../../aspose.words/documentbuilder/endbookmark/)(*string*) | Belgedeki geçerli konumu yer imi sonu olarak işaretler. |
| [EndColumnBookmark](../../aspose.words/documentbuilder/endcolumnbookmark/)(*string*) | Belgedeki geçerli konumu bir sütun yer imi sonu olarak işaretler. Konum bir tablo hücresinde olmalıdır. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange)() | Belgedeki geçerli konumu düzenlenebilir aralık sonu olarak işaretler. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange_1)(*[EditableRangeStart](../editablerangestart/)*) | Belgedeki geçerli konumu düzenlenebilir aralık sonu olarak işaretler. |
| [EndRow](../../aspose.words/documentbuilder/endrow/)() | Belgedeki bir tablo satırını sonlandırır. |
| [EndTable](../../aspose.words/documentbuilder/endtable/)() | Belgedeki bir tabloyu sonlandırır. |
| [InsertBreak](../../aspose.words/documentbuilder/insertbreak/)(*[BreakType](../breaktype/)*) | Belgeye belirtilen türde bir kesme ekler. |
| [InsertCell](../../aspose.words/documentbuilder/insertcell/)() | Belgeye bir tablo hücresi ekler. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_2)(*[ChartType](../../aspose.words.drawing.charts/charttype/), double, double*) | Belgeye bir grafik nesnesi ekler ve belirtilen boyuta ölçekler. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_3)(*[ChartType](../../aspose.words.drawing.charts/charttype/), double, double, [ChartStyle](../../aspose.words.drawing.charts/chartstyle/)*) | Belgeye bir grafik nesnesi ekler ve belirtilen boyuta ölçekler. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart)(*[ChartType](../../aspose.words.drawing.charts/charttype/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Belgeye bir grafik nesnesi ekler ve belirtilen boyuta ölçekler. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_1)(*[ChartType](../../aspose.words.drawing.charts/charttype/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/), [ChartStyle](../../aspose.words.drawing.charts/chartstyle/)*) | Belgeye bir grafik nesnesi ekler ve belirtilen boyuta ölçekler. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox_1)(*string, bool, int*) | Geçerli konuma bir onay kutusu form alanı ekler. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox)(*string, bool, bool, int*) | Geçerli konuma bir onay kutusu form alanı ekler. |
| [InsertComboBox](../../aspose.words/documentbuilder/insertcombobox/)(*string, string[], int*) | Geçerli konuma bir açılır kutu form alanı ekler. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument)(*[Document](../document/), [ImportFormatMode](../importformatmode/)*) | İmleç konumuna bir belge ekler. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument_1)(*[Document](../document/), [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | İmleç konumuna bir belge ekler. |
| [InsertDocumentInline](../../aspose.words/documentbuilder/insertdocumentinline/)(*[Document](../document/), [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | İmleç konumuna satır içi bir belge ekler. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_1)(*string*) | Bir Word alanını bir belgeye ekler ve alan sonucunu günceller. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool*) | Bir Word alanını bir belgeye ekler ve isteğe bağlı olarak alan sonucunu günceller. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_2)(*string, string*) | Alan sonucunu güncellemeden bir Word alanını belgeye ekler. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote)(*[FootnoteType](../../aspose.words.notes/footnotetype/), string*) | Belgeye dipnot veya sonnot ekler. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote_1)(*[FootnoteType](../../aspose.words.notes/footnotetype/), string, string*) | Belgeye dipnot veya sonnot ekler. |
| [InsertForms2OleControl](../../aspose.words/documentbuilder/insertforms2olecontrol/)(*[Forms2OleControl](../../aspose.words.drawing.ole/forms2olecontrol/)*) | Ekler[`Forms2OleControl`](../../aspose.words.drawing.ole/forms2olecontrol/) nesneyi geçerli konuma taşı. |
| [InsertGroupShape](../../aspose.words/documentbuilder/insertgroupshape/#insertgroupshape)(*params ShapeBase[]*) | Parametre olarak geçirilen şekilleri, geçerli konuma eklenen yeni bir GroupShape düğümüne gruplandırır. |
| [InsertGroupShape](../../aspose.words/documentbuilder/insertgroupshape/#insertgroupshape_1)(*double, double, double, double, params ShapeBase[]*) | Belirtilen boyuttaki yeni bir GroupShape düğümüne parametre olarak geçirilen şekilleri gruplandırır ve belirtilen konuma eklenir. |
| [InsertHorizontalRule](../../aspose.words/documentbuilder/inserthorizontalrule/)() | Belgeye yatay bir kural şekli ekler. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml)(*string*) | Belgeye bir HTML dizesi ekler. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_2)(*string, bool*) | Belgeye bir HTML dizesi ekler. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_1)(*string, [HtmlInsertOptions](../htmlinsertoptions/)*) | Belgeye bir HTML dizesi ekler. Ek seçeneklerin belirtilmesine olanak tanır. |
| [InsertHyperlink](../../aspose.words/documentbuilder/inserthyperlink/)(*string, string, bool*) | Belgeye bir köprü metni ekler. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage)(*byte[]*) | Bir bayt dizisinden belgeye bir görüntü ekler. Görüntü satır içi ve %100 ölçekte eklenir. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_3)(*Image*) | .NET'ten bir görüntü eklerImage nesnesini belgeye ekleyin. Görüntü satır içi ve %100 ölçekte eklenir. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_6)(*Stream*) | Bir akıştan belgeye bir görüntü ekler. Görüntü satır içi ve %100 ölçekte eklenir. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_9)(*string*) | Bir dosyadan veya URL'den belgeye bir resim ekler. Resim satır içi ve %100 ölçekte eklenir. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_2)(*byte[], double, double*) | Bir bayt dizisinden belgeye satır içi bir resim ekler ve belirtilen boyuta ölçekler. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_5)(*Image, double, double*) | .NET'ten satır içi bir resim eklerImage nesnesini belgeye ekler ve belirtilen boyuta ölçekler. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_8)(*Stream, double, double*) | Bir akıştan belgeye satır içi bir resim ekler ve belirtilen boyuta ölçekler. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_11)(*string, double, double*) | Bir dosyadan veya URL'den belgeye satır içi bir resim ekler ve belirtilen boyuta ölçekler. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_1)(*byte[], [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Belirtilen konum ve boyutta bir bayt dizisinden bir resim ekler. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_4)(*Image, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | .NET'ten bir görüntü eklerImage Belirtilen konum ve boyutta nesnesi. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_7)(*Stream, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Belirtilen konum ve boyutta bir akıştan bir görüntü ekler. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_10)(*string, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Belirtilen konuma ve boyuta bir dosyadan veya URL'den bir resim ekler. |
| [InsertNode](../../aspose.words/documentbuilder/insertnode/)(*[Node](../node/)*) | İmlecin önüne bir düğüm ekler. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject)(*Stream, string, bool, Stream*) | Bir akıştan gömülü bir OLE nesnesini belgeye ekler. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_1)(*string, bool, bool, Stream*) | Bir dosyadan belgeye gömülü veya bağlantılı bir OLE nesnesi ekler. Dosya uzantısını kullanarak OLE nesne türünü algılar. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_2)(*string, string, bool, bool, Stream*) | Bir dosyadan gömülü veya bağlantılı bir OLE nesnesini belgeye ekler. Belirtilen progID parametresini kullanarak OLE nesne türünü algılar. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon)(*Stream, string, string, string*) | Bir akıştan belgeye simge olarak gömülü bir OLE nesnesi ekler. Simge dosyasını ve başlığı belirtmeye izin verir. Belirtilen progID parametresini kullanarak OLE nesne türünü algılar. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_1)(*string, bool, string, string*) | Belgeye simge olarak gömülü veya bağlantılı bir OLE nesnesi ekler. Simge dosyasını ve başlığı belirtmeye izin verir. Dosya uzantısını kullanarak OLE nesne türünü algılar. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_2)(*string, string, bool, string, string*) | Belgeye simge olarak gömülü veya bağlantılı bir OLE nesnesi ekler. Simge dosyasını ve başlığı belirtmeye izin verir. Belirtilen progID parametresini kullanarak OLE nesne türünü algılar. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_1)(*string, double, double*) | Belgeye çevrimiçi bir video nesnesi ekler ve belirtilen boyuta ölçekler. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_3)(*string, string, byte[], double, double*) | Belgeye çevrimiçi bir video nesnesi ekler ve belirtilen boyuta ölçekler. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo)(*string, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Belgeye çevrimiçi bir video nesnesi ekler ve belirtilen boyuta ölçekler. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_2)(*string, string, byte[], [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Belgeye çevrimiçi bir video nesnesi ekler ve belirtilen boyuta ölçekler. |
| [InsertParagraph](../../aspose.words/documentbuilder/insertparagraph/)() | Belgeye bir paragraf sonu ekler. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape_1)(*[ShapeType](../../aspose.words.drawing/shapetype/), double, double*) | Belirtilen tür ve boyutta satır içi şekil ekler. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape)(*[ShapeType](../../aspose.words.drawing/shapetype/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Belirtilen konum, boyut ve metin kaydırma türüyle serbest yüzen şekil ekler. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline)(*[SignatureLineOptions](../signaturelineoptions/)*) | Geçerli konuma bir imza satırı ekler. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline_1)(*[SignatureLineOptions](../signaturelineoptions/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Belirtilen konuma bir imza satırı ekler. |
| [InsertStructuredDocumentTag](../../aspose.words/documentbuilder/insertstructureddocumenttag/)(*[SdtType](../../aspose.words.markup/sdttype/)*) | Bir ekler[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) belgeye. |
| [InsertStyleSeparator](../../aspose.words/documentbuilder/insertstyleseparator/)() | Belgeye stil ayırıcı ekler. |
| [InsertTableOfContents](../../aspose.words/documentbuilder/inserttableofcontents/)(*string*) | Belgeye bir TOC (içindekiler tablosu) alanı ekler. |
| [InsertTextInput](../../aspose.words/documentbuilder/inserttextinput/)(*string, [TextFormFieldType](../../aspose.words.fields/textformfieldtype/), string, string, int*) | Geçerli konuma bir metin formu alanı ekler. |
| [MoveTo](../../aspose.words/documentbuilder/moveto/)(*[Node](../node/)*) | İmleci satır içi bir düğüme veya bir paragrafın sonuna taşır. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark)(*string*) | İmleci bir yer imine taşır. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark_1)(*string, bool, bool*) | İmleci daha büyük bir hassasiyetle bir yer imine taşır. |
| [MoveToCell](../../aspose.words/documentbuilder/movetocell/)(*int, int, int, int*) | İmleci geçerli bölümdeki bir tablo hücresine taşır. |
| [MoveToDocumentEnd](../../aspose.words/documentbuilder/movetodocumentend/)() | İmleci belgenin sonuna taşır. |
| [MoveToDocumentStart](../../aspose.words/documentbuilder/movetodocumentstart/)() | İmleci belgenin başına taşır. |
| [MoveToField](../../aspose.words/documentbuilder/movetofield/)(*[Field](../../aspose.words.fields/field/), bool*) | İmleci belgedeki bir alana taşır. |
| [MoveToHeaderFooter](../../aspose.words/documentbuilder/movetoheaderfooter/)(*[HeaderFooterType](../headerfootertype/)*) | İmleci geçerli bölümdeki bir üstbilgi veya altbilginin başına taşır. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield)(*string*) | İmleci belirtilen birleştirme alanının hemen ötesine taşır ve birleştirme alanını kaldırır. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield_1)(*string, bool, bool*) | Birleştirme alanını belirtilen birleştirme alanına taşır. |
| [MoveToParagraph](../../aspose.words/documentbuilder/movetoparagraph/)(*int, int*) | İmleci geçerli bölümdeki bir paragrafa taşır. |
| [MoveToSection](../../aspose.words/documentbuilder/movetosection/)(*int*) | İmleci belirtilen bölümdeki gövdenin başına taşır. |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag_1)(*int, int*) | İmleci geçerli bölümdeki yapılandırılmış bir belge etiketine taşır. |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag)(*[StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/), int*) | İmleci yapılandırılmış belge etiketine taşır. |
| [PopFont](../../aspose.words/documentbuilder/popfont/)() | Yığında daha önce kaydedilmiş karakter biçimlendirmesini alır. |
| [PushFont](../../aspose.words/documentbuilder/pushfont/)() | Mevcut karakter biçimlendirmesini yığına kaydeder. |
| [StartBookmark](../../aspose.words/documentbuilder/startbookmark/)(*string*) | Belgedeki geçerli konumu yer imi başlangıcı olarak işaretler. |
| [StartColumnBookmark](../../aspose.words/documentbuilder/startcolumnbookmark/)(*string*) | Belgedeki geçerli konumu bir sütun yer imi başlangıcı olarak işaretler. Konum bir tablo hücresinde olmalıdır. |
| [StartEditableRange](../../aspose.words/documentbuilder/starteditablerange/)() | Belgedeki geçerli konumu düzenlenebilir bir aralık başlangıcı olarak işaretler. |
| [StartTable](../../aspose.words/documentbuilder/starttable/)() | Belgede bir tablo başlatır. |
| [Write](../../aspose.words/documentbuilder/write/)(*string*) | Belgeye geçerli ekleme konumuna bir dize ekler. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln)() | Belgeye bir paragraf sonu ekler. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln_1)(*string*) | Belgeye bir dize ve bir paragraf sonu ekler. |

## Notlar

`DocumentBuilder` bir yapı inşa etme sürecini kolaylaştırır[`Document`](../document/) daha kolay. [`Document`](../document/) düğümlerden oluşan bir ağaçtan oluşan bileşik bir nesnedir ve content düğümlerini doğrudan ağaca eklemek mümkün olsa da, ağaç yapısının iyi anlaşılmasını gerektirir. `DocumentBuilder` karmaşık yapının bir "cephesi"dir[`Document`](../document/) ve allows içeriği ve biçimlendirmeyi hızlı ve kolay bir şekilde eklemesine olanak tanır.

Bir tane oluştur`DocumentBuilder` ve onu bir şeyle ilişkilendir[`Document`](../document/).

The`DocumentBuilder` çağırdığınızda metnin ekleneceği dahili bir imleç vardır [`Write`](./write/) ,[`Writeln`](./writeln/) ,[`InsertBreak`](./insertbreak/) ve diğer yöntemler. Gezinebilirsiniz`DocumentBuilder` Çeşitli MoveToXXX yöntemlerini kullanarak bir belgedeki farklı bir location konumuna imleç.

Kullanın[`Font`](./font/) to belgedeki geçerli konumdan itibaren eklenen tüm metne uygulanacak karakter biçimlendirmesini belirten özellik.

Kullanın[`ParagraphFormat`](./paragraphformat/) current ve eklenecek tüm paragraflar için paragraf biçimlendirmesini belirtmek için kullanılan özellik.

Kullanın[`PageSetup`](./pagesetup/) current bölümü ve eklenecek tüm bölümler için sayfa ve bölüm özelliklerini belirtmek için kullanılan özellik.

Kullanın[`CellFormat`](./cellformat/) Ve[`RowFormat`](./rowformat/) özellikleri belirtmek için tablo hücreleri ve satırları için biçimlendirme özellikleri. Kullanıcı[`InsertCell`](./insertcell/) ve [`EndRow`](./endrow/) Bir tablo oluşturmanın yöntemleri.

Dikkat[`Font`](./font/) ,[`ParagraphFormat`](./paragraphformat/) Ve[`PageSetup`](./pagesetup/) Belgede farklı bir yere gittiğinizde biçimlendirme özelliklerinin yeni konumda kullanılabilmesini sağlamak için özellikler her zaman güncellenir.

## Örnekler

Bir tablo oluşturmak için belge oluşturucunun nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Tabloyu başlatın, ardından ilk satırı iki hücreyle doldurun.
builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");

// Yeni bir satır başlatmak için oluşturucunun "EndRow" metodunu çağırın.
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateTable.docx");
```

DocumentBuilder kullanılarak bir belgede üstbilgi ve altbilgilerin nasıl oluşturulacağını gösterir.

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

Özel kenarlıkları olan bir tablonun nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Bir belge oluşturucu için tablo biçimlendirme seçeneklerini ayarlama
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

// Biçimlendirmeyi değiştirmek, bunu geçerli hücreye uygulayacaktır.
// ve sonrasında builder ile oluşturduğumuz yeni hücreler.
// Bu daha önce eklediğimiz hücreleri etkilemeyecektir.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Dikey metne uyacak şekilde satır yüksekliğini artırın.
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
