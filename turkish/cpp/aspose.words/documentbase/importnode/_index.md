---
title: "Aspose::Words::DocumentBase::ImportNode yöntemi"
linktitle: "ImportNode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBase::ImportNode yöntemi. C++'da başka bir belgeden bir düğümü geçerli belgeye aktarır."
type: docs
weight: 12000
url: /tr/cpp/aspose.words/documentbase/importnode/
---
## DocumentBase::ImportNode(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Başka bir belgeden bir düğümü geçerli belgeye aktarır.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBase::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Aktarılacak düğüm. |
| isImportChildren | bool | **true** tüm alt düğümleri özyinelemeli olarak içe aktarmak için; aksi takdirde **false**. |

### ReturnValue

Mevcut belgeye ait kopyalanmış düğüm.
## Açıklamalar


Bu yöntem, biçimlendirmeyi çözmek için [UseDestinationStyles](../../importformatmode/) seçeneğini kullanır.

Bir düğümü içe aktarmak, içe aktaran belgeye ait kaynak düğümün bir kopyasını oluşturur. Döndürülen düğümün ebeveyni yoktur. Kaynak düğüm, orijinal belgede değiştirilmez veya kaldırılmaz.

Başka bir belgeden bir düğüm bu belgeye eklenebilmeden önce, içe aktarılması gerekir. İçe aktarma sırasında, stillere ve listelere referanslar gibi belgeye özgü özellikler orijinalden içe aktaran belgeye çevrilir. Düğüm içe aktarıldıktan sonra, belge içinde uygun konuma [InsertBefore1()</see> veya <see cref="Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertAfter1()](../) kullanılarak eklenebilir.

Kaynak düğüm zaten hedef belgeye aitse, sadece kaynak düğümün derin bir kopyası oluşturulur.

## Örnekler



Bir düğümün bir belgeden diğerine nasıl içe aktarılacağını gösterir.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto dstDoc = System::MakeObject<Aspose::Words::Document>();

srcDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(srcDoc, u"Source document first paragraph text."));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(dstDoc, u"Destination document first paragraph text."));

// Her düğümün içinde bulunduğu belge olan bir üst belge vardır.
// Düğümün ait olmadığı bir belgeye düğüm eklemek bir istisna (exception) fırlatır.
ASPOSE_ASSERT_NE(dstDoc, srcDoc->get_FirstSection()->get_Document());
ASSERT_THROW(static_cast<std::function<void()>>([&dstDoc, &srcDoc]() -> void
{
    dstDoc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(srcDoc->get_FirstSection());
})(), System::ArgumentException);

// ImportNode yöntemini kullanarak bir düğümün kopyasını oluşturun; bu kopya belgeyi alacaktır.
// ImportNode yöntemini çağıran belgeyi yeni sahibi belge olarak ayarlar.
auto importedSection = System::ExplicitCast<Aspose::Words::Section>(dstDoc->ImportNode(srcDoc->get_FirstSection(), true));

ASPOSE_ASSERT_EQ(dstDoc, importedSection->get_Document());

// Artık düğümü belgeye ekleyebiliriz.
dstDoc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(importedSection);

ASSERT_EQ(u"Destination document first paragraph text.\r\nSource document first paragraph text.\r\n", dstDoc->ToString(Aspose::Words::SaveFormat::Text));
```

## Ayrıca Bakınız

* Class [Node](../../node/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBase::ImportNode(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) method


Başka bir belgeden bir düğümü, biçimlendirmeyi kontrol etme seçeneğiyle geçerli belgeye aktarır.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBase::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren, Aspose::Words::ImportFormatMode importFormatMode)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | İçe aktarılacak düğüm. |
| isImportChildren | bool | **true** tüm alt düğümleri özyinelemeli olarak içe aktarmak için; aksi takdirde **false**. |
| importFormatMode | Aspose::Words::ImportFormatMode | Çakışan stil biçimlendirmesinin nasıl birleştirileceğini belirtir. |

### ReturnValue

Kopyalanmış, içe aktarılmış düğüm. Düğüm hedef belgeye aittir, ancak ebeveyni yoktur.
## Açıklamalar


Bu aşırı yükleme, stillerin ve liste biçimlendirmesinin nasıl içe aktarılacağını kontrol etmek için kullanışlıdır.

Bir düğümü içe aktarmak, içe aktaran belgeye ait kaynak düğümün bir kopyasını oluşturur. Döndürülen düğümün ebeveyni yoktur. Kaynak düğüm, orijinal belgede değiştirilmez veya kaldırılmaz.

Başka bir belgeden bir düğüm bu belgeye eklenebilmeden önce, içe aktarılması gerekir. İçe aktarma sırasında, stillere ve listelere referanslar gibi belgeye özgü özellikler orijinalden içe aktaran belgeye çevrilir. Düğüm içe aktarıldıktan sonra, belge içinde uygun konuma [InsertBefore1()</see> veya <see cref="Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertAfter1()](../) kullanılarak eklenebilir.

Kaynak düğüm zaten hedef belgeye aitse, sadece kaynak düğümün derin bir kopyası oluşturulur.

## Örnekler



Belirli seçeneklerle kaynak belgeden hedef belgeye düğümün nasıl içe aktarılacağını gösterir.
```cpp
// İki belge oluşturun ve her belgeye bir karakter stili ekleyin.
// Stilleri aynı ada sahip olacak şekilde, ancak farklı metin biçimlendirmesiyle yapılandırın.
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> srcStyle = srcDoc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"My style");
srcStyle->get_Font()->set_Name(u"Courier New");
auto srcBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);
srcBuilder->get_Font()->set_Style(srcStyle);
srcBuilder->Writeln(u"Source document text.");

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> dstStyle = dstDoc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"My style");
dstStyle->get_Font()->set_Name(u"Calibri");
auto dstBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
dstBuilder->get_Font()->set_Style(dstStyle);
dstBuilder->Writeln(u"Destination document text.");

// Stil adı çakışmasına neden olarak, hedef belgeden bölümü (Section) kaynak belgeye içe aktarın.
// Eğer hedef stilleri kullanırsak, aynı stil adına sahip içe aktarılmış kaynak metin
// hedef metin gibi hedef stilini benimseyecektir.
auto importedSection = System::ExplicitCast<Aspose::Words::Section>(dstDoc->ImportNode(srcDoc->get_FirstSection(), true, Aspose::Words::ImportFormatMode::UseDestinationStyles));
ASSERT_EQ(dstStyle->get_Font()->get_Name(), importedSection->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());
ASSERT_EQ(dstStyle->get_Name(), importedSection->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_StyleName());

// ImportFormatMode.KeepDifferentStyles kullanırsak, kaynak stil korunur,
// ve ad çakışması bir ek (suffix) eklenerek çözülür.
dstDoc->ImportNode(srcDoc->get_FirstSection(), true, Aspose::Words::ImportFormatMode::KeepDifferentStyles);
ASSERT_EQ(dstStyle->get_Font()->get_Name(), dstDoc->get_Styles()->idx_get(u"My style")->get_Font()->get_Name());
ASSERT_EQ(srcStyle->get_Font()->get_Name(), dstDoc->get_Styles()->idx_get(u"My style_0")->get_Font()->get_Name());
```

## Ayrıca Bakınız

* Class [Node](../../node/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBase::ImportNode(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) method


Başka bir belgeden bir düğümü, biçimlendirmeyi kontrol etme seçeneğiyle geçerli belgeye aktarır.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBase::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | İçe aktarılacak düğüm. |
| isImportChildren | bool | **true** tüm alt düğümleri özyinelemeli olarak içe aktarmak için; aksi takdirde **false**. |
| importFormatMode | Aspose::Words::ImportFormatMode | Çakışan stil biçimlendirmesinin nasıl birleştirileceğini belirtir. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Çeşitli ek biçimlendirme seçeneklerini belirtmeye olanak tanır. |

### ReturnValue

Kopyalanmış, içe aktarılmış düğüm. Düğüm hedef belgeye aittir, ancak ebeveyni yoktur.
## Açıklamalar


Bu aşırı yükleme, stillerin ve liste biçimlendirmesinin nasıl içe aktarılacağını kontrol etmek için kullanışlıdır.

Bir düğümü içe aktarmak, içe aktaran belgeye ait kaynak düğümün bir kopyasını oluşturur. Döndürülen düğümün ebeveyni yoktur. Kaynak düğüm, orijinal belgede değiştirilmez veya kaldırılmaz.

Başka bir belgeden bir düğüm bu belgeye eklenebilmeden önce, içe aktarılması gerekir. İçe aktarma sırasında, stillere ve listelere referanslar gibi belgeye özgü özellikler orijinalden içe aktaran belgeye çevrilir. Düğüm içe aktarıldıktan sonra, belge içinde uygun konuma [InsertBefore1()</see> veya <see cref="Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertAfter1()](../) kullanılarak eklenebilir.

Kaynak düğüm zaten hedef belgeye aitse, sadece kaynak düğümün derin bir kopyası oluşturulur.

## Örnekler



Şekillerin kaynak tema renklerini çözümlerek bir düğümün nasıl içe aktarılacağını gösterir.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);

// Birincil altbilgiye gidin ve tema renklerini kullanan bir şekil ekleyin.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 50);
shape->get_Stroke()->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
// Tema renkleri çözümlenmiş şekilde kaynak altbilgiyi hedef belgeye aktarın,
// böylece şekil, kaynak belgeden gerçek rengini korur.
System::SharedPtr<Aspose::Words::HeaderFooter> footer = srcDoc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ResolveThemeColors(true);
auto importedFooter = System::ExplicitCast<Aspose::Words::HeaderFooter>(dstDoc->ImportNode(footer, true, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options));

dstDoc->get_FirstSection()->get_HeadersFooters()->Add(importedFooter);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBase.ImportNodeWithResolveThemeColors.docx");
```

## Ayrıca Bakınız

* Class [Node](../../node/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
