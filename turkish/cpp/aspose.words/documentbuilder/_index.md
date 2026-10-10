---
title: "Aspose::Words::DocumentBuilder class"
linktitle: "DocumentBuilder"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder sınıfı. Metin, görüntü ve diğer içerikleri eklemek, yazı tipi, paragraf ve bölüm biçimlendirmesini belirtmek için yöntemler sağlar. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 22000
url: /tr/cpp/aspose.words/documentbuilder/
---
## DocumentBuilder class


Metin, resim ve diğer içerikleri eklemek, yazı tipi, paragraf ve bölüm biçimlendirmesini belirtmek için yöntemler sağlar. Daha fazla bilgi edinmek için [Document Builder Overview](https://docs.aspose.com/words/cpp/document-builder-overview/) dokümantasyon makalesini ziyaret edin.

```cpp
class DocumentBuilder : public Aspose::Words::IRunAttrSource,
                        public Aspose::Words::IParaAttrSource,
                        public Aspose::Words::IRowAttrSource,
                        public Aspose::Words::ICellAttrSource
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [DeleteRow](./deleterow/)(int32_t, int32_t) | Bir tablodan bir satırı siler. |
| [DocumentBuilder](./documentbuilder/)() | Bu sınıfın yeni bir örneğini başlatır. |
| [DocumentBuilder](./documentbuilder/)(const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) | Bu sınıfın yeni bir örneğini başlatır. |
| [DocumentBuilder](./documentbuilder/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Bu sınıfın yeni bir örneğini başlatır. |
| [DocumentBuilder](./documentbuilder/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) | Bu sınıfın yeni bir örneğini başlatır. |
| [EndBookmark](./endbookmark/)(const System::String\&) | Belgedeki mevcut konumu bir yer imi sonu olarak işaretler. |
| [EndColumnBookmark](./endcolumnbookmark/)(const System::String\&) | Belgedeki mevcut konumu bir sütun yer imi sonu olarak işaretler. Konum bir tablo hücresinde olmalıdır. |
| [EndEditableRange](./endeditablerange/)() | Belgedeki mevcut konumu düzenlenebilir bir aralık sonu olarak işaretler. |
| [EndEditableRange](./endeditablerange/)(const System::SharedPtr\<Aspose::Words::EditableRangeStart\>\&) | Belgedeki mevcut konumu düzenlenebilir bir aralık sonu olarak işaretler. |
| [EndRow](./endrow/)() | Belgede bir tablo satırını sonlandırır. |
| [EndTable](./endtable/)() | Belgede bir tabloyu sonlandırır. |
| [get_Bold](./get_bold/)() | Yazı tipi kalın olarak biçimlendirilmişse doğru. |
| [get_CellFormat](./get_cellformat/)() | Geçerli tablo hücresi biçimlendirme özelliklerini temsil eden bir nesne döndürür. |
| [get_CurrentNode](./get_currentnode/)() | Bu [DocumentBuilder](./) içinde şu anda seçili olan düğümü alır. |
| [get_CurrentParagraph](./get_currentparagraph/)() | Bu [DocumentBuilder](./) içinde şu anda seçili olan paragrafı alır. |
| [get_CurrentSection](./get_currentsection/)() | Bu [DocumentBuilder](./) içinde şu anda seçili olan bölümü alır. |
| [get_CurrentStory](./get_currentstory/)() | Bu [DocumentBuilder](./) içinde şu anda seçili olan hikayeyi alır. |
| [get_CurrentStructuredDocumentTag](./get_currentstructureddocumenttag/)() | Bu [DocumentBuilder](./) içinde şu anda seçili olan yapılandırılmış belge etiketini alır. |
| [get_Document](./get_document/)() const | Bu nesnenin bağlı olduğu [Document](./get_document/) nesnesini alır veya ayarlar. |
| [get_Font](./get_font/)() | Geçerli yazı tipi biçimlendirme özelliklerini temsil eden bir nesne döndürür. |
| [get_IsAtEndOfParagraph](./get_isatendofparagraph/)() | İmleç mevcut paragrafın sonunda ise **true** döndürür. |
| [get_IsAtEndOfStructuredDocumentTag](./get_isatendofstructureddocumenttag/)() | İmleç yapılandırılmış belge etiketinin sonunda ise **true** döndürür. |
| [get_IsAtStartOfParagraph](./get_isatstartofparagraph/)() | İmleç mevcut paragrafın başında ise (imleçten önce metin yok) **true** döndürür. |
| [get_Italic](./get_italic/)() | Yazı tipi italik olarak biçimlendirilmişse Doğru. |
| [get_ListFormat](./get_listformat/)() | Geçerli liste biçimlendirme özelliklerini temsil eden bir nesne döndürür. |
| [get_PageSetup](./get_pagesetup/)() | Geçerli sayfa ayarı ve bölüm özelliklerini temsil eden bir nesne döndürür. |
| [get_ParagraphFormat](./get_paragraphformat/)() | Geçerli paragraf biçimlendirme özelliklerini temsil eden bir nesne döndürür. |
| [get_RowFormat](./get_rowformat/)() | Geçerli tablo satırı biçimlendirme özelliklerini temsil eden bir nesne döndürür. |
| [get_Underline](./get_underline/)() | Geçerli yazı tipi için alt çizgi tipini alır/ayarlar. |
| [GetType](./gettype/)() const override |  |
| [InsertBreak](./insertbreak/)(Aspose::Words::BreakType) | Belgeye belirtilen türde bir kesme ekler. |
| [InsertCell](./insertcell/)() | Belgeye bir tablo hücresi ekler. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, double, double) | Belgeye bir grafik nesnesi ekler ve belirtilen boyuta ölçeklendirir. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, double, double, Aspose::Words::Drawing::Charts::ChartStyle) | Belgeye bir grafik nesnesi ekler ve belirtilen boyuta ölçeklendirir. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Belgeye bir grafik nesnesi ekler ve belirtilen boyuta ölçeklendirir. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType, Aspose::Words::Drawing::Charts::ChartStyle) | Belgeye bir grafik nesnesi ekler ve belirtilen boyuta ölçeklendirir. |
| [InsertCheckBox](./insertcheckbox/)(const System::String\&, bool, int32_t) | Geçerli konuma bir onay kutusu form alanı ekler. |
| [InsertCheckBox](./insertcheckbox/)(const System::String\&, bool, bool, int32_t) | Geçerli konuma bir onay kutusu form alanı ekler. |
| [InsertComboBox](./insertcombobox/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, int32_t) | Geçerli konuma bir açılır kutu form alanı ekler. |
| [InsertDocument](./insertdocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode) | İmleç konumuna bir belge ekler. |
| [InsertDocument](./insertdocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | İmleç konumuna bir belge ekler. |
| [InsertDocumentInline](./insertdocumentinline/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | İmleç konumunda belgeyi satır içi ekler. |
| [InsertField](./insertfield/)(Aspose::Words::Fields::FieldType, bool) | Bir belgeye Word alanı ekler ve isteğe bağlı olarak alan sonucunu günceller. |
| [InsertField](./insertfield/)(const System::String\&) | Bir belgeye Word alanı ekler ve alan sonucunu günceller. |
| [InsertField](./insertfield/)(const System::String\&, const System::String\&) | Bir belgeye Word alanı ekler ve alan sonucunu güncellemez. |
| [InsertFootnote](./insertfootnote/)(Aspose::Words::Notes::FootnoteType, const System::String\&) | Belgeye bir dipnot veya sonnot ekler. |
| [InsertFootnote](./insertfootnote/)(Aspose::Words::Notes::FootnoteType, const System::String\&, const System::String\&) | Belgeye bir dipnot veya sonnot ekler. |
| [InsertForms2OleControl](./insertforms2olecontrol/)(const System::SharedPtr\<Aspose::Words::Drawing::Ole::Forms2OleControl\>\&) | Geçerli konuma [Forms2OleControl](../) nesnesi ekler. |
| [InsertGroupShape](./insertgroupshape/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) | Parametre olarak verilen şekilleri yeni bir GroupShape düğümüne gruplar ve bu düğüm geçerli konuma eklenir. |
| [InsertGroupShape](./insertgroupshape/)(double, double, double, double, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) | Parametre olarak verilen şekilleri belirtilen boyutta yeni bir GroupShape düğümüne gruplar ve bu düğüm belirtilen konuma eklenir. |
| [InsertHorizontalRule](./inserthorizontalrule/)() | Belgeye yatay kural şekli ekler. |
| [InsertHtml](./inserthtml/)(const System::String\&) | Belgeye bir HTML dizesi ekler. |
| [InsertHtml](./inserthtml/)(const System::String\&, bool) | Belgeye bir HTML dizesi ekler. |
| [InsertHtml](./inserthtml/)(const System::String\&, Aspose::Words::HtmlInsertOptions) | Belgeye bir HTML dizesi ekler. Ek seçenekleri belirtmeye izin verir. |
| [InsertHyperlink](./inserthyperlink/)(const System::String\&, const System::String\&, bool) | Belgeye bir köprü ekler. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::Drawing::Image\>\&) | **Image** nesnesinden bir görüntü belgeye ekler. Görüntü satır içi ve %100 ölçekle eklenir. |
| [InsertImage](./insertimage/)(const System::String\&) | Bir dosya veya URL'den bir görüntüyü belgeye ekler. Görüntü satır içi ve %100 ölçekle eklenir. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::IO::Stream\>\&) | Bir akıştan bir görüntüyü belgeye ekler. Görüntü satır içi ve %100 ölçekle eklenir. |
| [InsertImage](./insertimage/)(const System::ArrayPtr\<uint8_t\>\&) | Bir bayt dizisinden bir görüntüyü belgeye ekler. Görüntü satır içi ve %100 ölçekle eklenir. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::Drawing::Image\>\&, double, double) | **Image** nesnesinden satır içi bir görüntüyü belgeye ekler ve belirtilen boyuta ölçeklendirir. |
| [InsertImage](./insertimage/)(const System::String\&, double, double) | Bir dosya veya URL'den satır içi bir görüntüyü belgeye ekler ve belirtilen boyuta ölçeklendirir. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::IO::Stream\>\&, double, double) | Bir akıştan satır içi bir görüntüyü belgeye ekler ve belirtilen boyuta ölçeklendirir. |
| [InsertImage](./insertimage/)(const System::ArrayPtr\<uint8_t\>\&, double, double) | Bir bayt dizisinden satır içi bir görüntüyü belgeye ekler ve belirtilen boyuta ölçeklendirir. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::Drawing::Image\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | **Image** nesnesinden belirtilen konum ve boyutta bir görüntü ekler. |
| [InsertImage](./insertimage/)(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Bir dosya veya URL'den belirtilen konum ve boyutta bir görüntü ekler. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Bir akıştan belirtilen konum ve boyutta bir görüntü ekler. |
| [InsertImage](./insertimage/)(const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Bir bayt dizisinden belirtilen konum ve boyutta bir görüntü ekler. |
| [InsertImage](./insertimage/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertImage](./insertimage/)(std::basic_istream\<CharType, Traits\>\&, double, double) |  |
| [InsertImage](./insertimage/)(std::basic_istream\<CharType, Traits\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) |  |
| [InsertNode](./insertnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | İmlecin önüne bir düğüm ekler. |
| [InsertOleObject](./insertoleobject/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, bool, const System::SharedPtr\<System::IO::Stream\>\&) | Bir akıştan gömülü bir OLE nesnesi belgeye ekler. |
| [InsertOleObject](./insertoleobject/)(const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) | Bir dosyadan gömülü veya bağlı bir OLE nesnesi belgeye ekler. OLE nesne tipini dosya uzantısı kullanarak algılar. |
| [InsertOleObject](./insertoleobject/)(const System::String\&, const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) | Bir dosyadan gömülü veya bağlı bir OLE nesnesi belgeye ekler. OLE nesne tipini verilen progID parametresi kullanarak algılar. |
| [InsertOleObject](./insertoleobject/)(std::basic_istream\<CharType, Traits\>\&, System::String, bool, std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertOleObject](./insertoleobject/)(System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertOleObject](./insertoleobject/)(System::String, System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(const System::String\&, bool, const System::String\&, const System::String\&) | Gömülü veya bağlı bir OLE nesnesini simge olarak belgeye ekler. Simge dosyasını ve başlığı belirtmeye izin verir. OLE nesne tipini dosya uzantısı kullanarak algılar. |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(const System::String\&, const System::String\&, bool, const System::String\&, const System::String\&) | Gömülü veya bağlı bir OLE nesnesini simge olarak belgeye ekler. Simge dosyasını ve başlığı belirtmeye izin verir. OLE nesne tipini verilen progID parametresi kullanarak algılar. |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, const System::String\&, const System::String\&) | Bir akıştan gömülü bir OLE nesnesini simge olarak belgeye ekler. Simge dosyasını ve başlığı belirtmeye izin verir. OLE nesne tipini verilen progID parametresi kullanarak algılar. |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(std::basic_istream\<CharType, Traits\>\&, System::String, System::String, System::String) |  |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, double, double) | Belgeye çevrimiçi bir video nesnesi ekler ve belirtilen boyuta ölçeklendirir. |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Belgeye çevrimiçi bir video nesnesi ekler ve belirtilen boyuta ölçeklendirir. |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, double, double) | Belgeye çevrimiçi bir video nesnesi ekler ve belirtilen boyuta ölçeklendirir. |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Belgeye çevrimiçi bir video nesnesi ekler ve belirtilen boyuta ölçeklendirir. |
| [InsertParagraph](./insertparagraph/)() | Belgeye bir paragraf sonu ekler. |
| [InsertShape](./insertshape/)(Aspose::Words::Drawing::ShapeType, double, double) | Belirtilen tip ve boyutta satır içi bir şekil ekler. |
| [InsertShape](./insertshape/)(Aspose::Words::Drawing::ShapeType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Belirtilen konum, boyut ve metin kaydırma tipiyle serbest yüzen bir şekil ekler. |
| [InsertSignatureLine](./insertsignatureline/)(const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\&) | Geçerli konuma bir imza satırı ekler. |
| [InsertSignatureLine](./insertsignatureline/)(const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, Aspose::Words::Drawing::WrapType) | Belirtilen konuma bir imza satırı ekler. |
| [InsertStructuredDocumentTag](./insertstructureddocumenttag/)(Aspose::Words::Markup::SdtType) | Belgeye bir [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/) ekler. |
| [InsertStyleSeparator](./insertstyleseparator/)() | Belgeye stil ayırıcı ekler. |
| [InsertTableOfContents](./inserttableofcontents/)(const System::String\&) | Belgeye bir TOC (içindekiler tablosu) alanı ekler. |
| [InsertTextInput](./inserttextinput/)(const System::String\&, Aspose::Words::Fields::TextFormFieldType, const System::String\&, const System::String\&, int32_t) | Geçerli konuma bir metin form alanı ekler. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MoveTo](./moveto/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | İmleci bir satır içi düğüme veya bir paragrafın sonuna taşır. |
| [MoveToBookmark](./movetobookmark/)(const System::String\&) | İmleci bir yer imine taşır. |
| [MoveToBookmark](./movetobookmark/)(const System::String\&, bool, bool) | İmleci daha yüksek hassasiyetle bir yer imine taşır. |
| [MoveToCell](./movetocell/)(int32_t, int32_t, int32_t, int32_t) | İmleci geçerli bölümdeki bir tablo hücresine taşır. |
| [MoveToDocumentEnd](./movetodocumentend/)() | İmleci belgenin sonuna taşır. |
| [MoveToDocumentStart](./movetodocumentstart/)() | İmleci belgenin başına taşır. |
| [MoveToField](./movetofield/)(const System::SharedPtr\<Aspose::Words::Fields::Field\>\&, bool) | İmleci belgede bir alana taşır. |
| [MoveToHeaderFooter](./movetoheaderfooter/)(Aspose::Words::HeaderFooterType) | İmleci geçerli bölümdeki bir üst bilgi ya da alt bilginin başına taşır. |
| [MoveToMergeField](./movetomergefield/)(const System::String\&) | İmleci belirtilen birleştirme alanının hemen sonrasına taşır ve birleştirme alanını kaldırır. |
| [MoveToMergeField](./movetomergefield/)(const System::String\&, bool, bool) | Birleştirme alanını belirtilen birleştirme alanına taşır. |
| [MoveToParagraph](./movetoparagraph/)(int32_t, int32_t) | İmleci geçerli bölümdeki bir paragrafa taşır. |
| [MoveToSection](./movetosection/)(int32_t) | İmleci belirtilen bölümdeki gövdenin başına taşır. |
| [MoveToStructuredDocumentTag](./movetostructureddocumenttag/)(int32_t, int32_t) | İmleci geçerli bölümdeki bir yapılandırılmış belge etiketine taşır. |
| [MoveToStructuredDocumentTag](./movetostructureddocumenttag/)(const System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>\&, int32_t) | İmleci yapılandırılmış belge etiketine taşır. |
| [PopFont](./popfont/)() | Yığına daha önce kaydedilen karakter biçimlendirmesini alır. |
| [PushFont](./pushfont/)() | Geçerli karakter biçimlendirmesini yığına kaydeder. |
| [set_Bold](./set_bold/)(bool) | Ayarlayıcı [Aspose::Words::DocumentBuilder::get_Bold](./get_bold/). |
| [set_Document](./set_document/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Ayarlayıcı [Aspose::Words::DocumentBuilder::get_Document](./get_document/). |
| [set_Italic](./set_italic/)(bool) | Ayarlayıcı [Aspose::Words::DocumentBuilder::get_Italic](./get_italic/). |
| [set_Underline](./set_underline/)(Aspose::Words::Underline) | [Aspose::Words::DocumentBuilder::get_Underline](./get_underline/) için ayarlayıcı. |
| [StartBookmark](./startbookmark/)(const System::String\&) | Belgedeki mevcut konumu bir yer imi başlangıcı olarak işaretler. |
| [StartColumnBookmark](./startcolumnbookmark/)(const System::String\&) | Belgedeki mevcut konumu bir sütun yer imi başlangıcı olarak işaretler. Konum bir tablo hücresinde olmalıdır. |
| [StartEditableRange](./starteditablerange/)() | Belgedeki mevcut konumu düzenlenebilir bir aralık başlangıcı olarak işaretler. |
| [StartTable](./starttable/)() | Belgede bir tablo başlatır. |
| static [Type](./type/)() |  |
| [Write](./write/)(const System::String\&) | Mevcut ekleme konumunda bir dizeyi belgeye ekler. |
| [Writeln](./writeln/)(const System::String\&) | Belgeye bir dize ve bir paragraf sonu ekler. |
| [Writeln](./writeln/)() | Belgeye bir paragraf sonu ekler. |
## Açıklamalar


[DocumentBuilder](./) makes the process of building a [Document](../document/) easier. [Document](../document/) is a composite object consisting of a tree of nodes and while inserting content nodes directly into the tree is possible, it requires good understanding of the tree structure. [DocumentBuilder](./) is a "facade" for the complex structure of [Document](../document/) and allows to insert content and formatting quickly and easily.

Bir [DocumentBuilder](./) oluşturun ve bir [Document](../document/) ile ilişkilendirin.

[DocumentBuilder](./) bir iç imlece sahiptir; [Write()](../), [Writeln()](../), [InsertBreak()](./insertbreak/) ve diğer yöntemleri çağırdığınızda metin bu imlece eklenir. Farklı MoveToXXX yöntemlerini kullanarak [DocumentBuilder](./) imlecini belgedeki başka bir konuma taşıyabilirsiniz.

Belgedeki mevcut konumdan itibaren eklenen tüm metne uygulanacak karakter biçimlendirmesini belirtmek için [Font](./get_font/) özelliğini kullanın.

Mevcut ve eklenecek tüm paragraflar için paragraf biçimlendirmesini belirtmek üzere [ParagraphFormat](./get_paragraphformat/) özelliğini kullanın.

Mevcut bölüm ve eklenecek tüm bölümler için sayfa ve bölüm özelliklerini belirtmek üzere [PageSetup](./get_pagesetup/) özelliğini kullanın.

Tablo hücreleri ve satırları için biçimlendirme özelliklerini belirtmek üzere [CellFormat](./get_cellformat/) ve [RowFormat](./get_rowformat/) özelliklerini kullanın. Bir tablo oluşturmak için [InsertCell](./insertcell/) ve [EndRow](./endrow/) yöntemlerini kullanın.

[Font](./get_font/), [ParagraphFormat](./get_paragraphformat/) ve [PageSetup](./get_pagesetup/) özelliklerinin, belge içinde farklı bir konuma geçtiğinizde yeni konumda mevcut olan biçimlendirme özelliklerini yansıtacak şekilde güncellendiğini unutmayın.

## Örnekler



Özel kenarlıklarla bir tablo oluşturmanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

// Bir DocumentBuilder için tablo biçimlendirme seçeneklerini ayarlama
// Bunları, onunla eklediğimiz her satır ve hücreye uygular.
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->set_Width(150);
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_GreenYellow());
builder->get_CellFormat()->set_WrapText(false);
builder->get_CellFormat()->set_FitText(true);

builder->get_RowFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_RowFormat()->set_Height(50);
builder->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Engrave3D);
builder->get_RowFormat()->get_Borders()->set_Color(System::Drawing::Color::get_Orange());

builder->InsertCell();
builder->Write(u"Row 1, Col 1");

builder->InsertCell();
builder->Write(u"Row 1, Col 2");
builder->EndRow();

// Biçimlendirmeyi değiştirmek, mevcut hücreye uygulanır,
// ve ardından builder ile oluşturduğumuz yeni hücrelere de.
// Bu, daha önce eklediğimiz hücreleri etkilemez.
builder->get_CellFormat()->get_Shading()->ClearFormatting();

builder->InsertCell();
builder->Write(u"Row 2, Col 1");

builder->InsertCell();
builder->Write(u"Row 2, Col 2");

builder->EndRow();

// Dikey metni sığdırmak için satır yüksekliğini artırın.
builder->InsertCell();
builder->get_RowFormat()->set_Height(150);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 3, Col 1");

builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 3, Col 2");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTable.docx");
```


Bir document builder kullanarak tablo oluşturmanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Tabloyu başlatın, ardından ilk satırı iki hücreyle doldurun.
builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2.");

// Call the builder's "EndRow" method to start a new row.
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 2.");
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateTable.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
