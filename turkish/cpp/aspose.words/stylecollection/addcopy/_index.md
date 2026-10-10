---
title: "Aspose::Words::StyleCollection::AddCopy metodu"
linktitle: "AddCopy"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::StyleCollection::AddCopy metodu. C++'ta bir stili bu koleksiyona kopyalar."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/stylecollection/addcopy/
---
## StyleCollection::AddCopy method


Bu koleksiyona bir stili kopyalar.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::AddCopy(const System::SharedPtr<Aspose::Words::Style> &style)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| style | const System::SharedPtr\<Aspose::Words::Style\>\& | [Style](../../style/) kopyalanacak. |

### ReturnValue

Kopyalanan stil kullanım için hazır.
## Açıklamalar


[Style](../../style/) to be copied can belong to the same document as well as to different document.

Bağlantılı stil kopyalandı.

Bu metod temel stilleri kopyalamaz.

Koleksiyon zaten aynı ada sahip bir stil içeriyorsa, yeni ad 0'dan başlayarak "_number" eki eklenerek otomatik olarak oluşturulur; ör. "Normal_0", "Heading 1_1" vb. İçe aktarılan stilin adını değiştirmek için [Name](../../style/get_name/) ayarlayıcısını kullanın.

## Örnekler



Bir belgenin stilinin nasıl klonlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// AddCopy yöntemi belirtilen stilin bir kopyasını oluşturur ve
// stil için otomatik olarak yeni bir ad oluşturur, örneğin "Heading 1_0".
System::SharedPtr<Aspose::Words::Style> newStyle = doc->get_Styles()->AddCopy(doc->get_Styles()->idx_get(u"Heading 1"));

// Stilin tanımlayıcı adını değiştirmek için stilin "Name" özelliğini kullanın.
newStyle->set_Name(u"My Heading 1");

// Belgemizde artık farklı adlara sahip iki aynı görünümlü stil var.
// Stillerden birinin ayarlarını değiştirmek diğerini etkilemez.
newStyle->get_Font()->set_Color(System::Drawing::Color::get_Red());

ASSERT_EQ(u"My Heading 1", newStyle->get_Name());
ASSERT_EQ(u"Heading 1", doc->get_Styles()->idx_get(u"Heading 1")->get_Name());

ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Type(), newStyle->get_Type());
ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Name(), newStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Size(), newStyle->get_Font()->get_Size());
ASPOSE_ASSERT_NE(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Color(), newStyle->get_Font()->get_Color());
```


Bir belgeden başka bir belgeye stil nasıl içe aktarılır gösterir.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();

// Kaynak belge için özel bir stil oluşturun.
System::SharedPtr<Aspose::Words::Style> srcStyle = srcDoc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
srcStyle->get_Font()->set_Color(System::Drawing::Color::get_Red());

// Kaynak belgenin özel stilini hedef belgeye içe aktarın.
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> newStyle = dstDoc->get_Styles()->AddCopy(srcStyle);

// İçe aktarılan stil, kaynak stiline aynı görünüme sahiptir.
ASSERT_EQ(u"MyStyle", newStyle->get_Name());
ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), newStyle->get_Font()->get_Color().ToArgb());
```

## Ayrıca Bakınız

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
