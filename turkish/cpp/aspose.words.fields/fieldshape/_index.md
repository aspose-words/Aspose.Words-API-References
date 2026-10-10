---
title: "Aspose::Words::Fields::FieldShape sınıfı"
linktitle: "FieldShape"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldShape sınıfı. SHAPE alanını uygular. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 93000
url: /tr/cpp/aspose.words.fields/fieldshape/
---
## FieldShape class


SHAPE alanını uygular. Daha fazla bilgi edinmek için [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokümantasyon makalesini ziyaret edin.

```cpp
class FieldShape : public Aspose::Words::Fields::Field
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Görüntülenen alan sonucunu temsil eden metni alır. |
| [get_End](../field/get_end/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldEnd](../field/get_fieldend/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldStart](../field/get_fieldstart/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_Format](../field/get_format/)() | Alan biçimlendirmesine tipli erişim sağlayan bir [FieldFormat](../fieldformat/) nesnesi alır. |
| [get_IsDirty](../field/get_isdirty/)() | Alan'ın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [get_IsLocked](../field/get_islocked/)() | Alan'ın kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) alır veya ayarlar. |
| [get_LocaleId](../field/get_localeid/)() | Alan'ın LCID'sini alır veya ayarlar. |
| [get_Result](../field/get_result/)() | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [get_Separator](../field/get_separator/)() | Alan ayırıcıyı temsil eden düğümü alır. **null** olabilir. |
| [get_Start](../field/get_start/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_Text](./get_text/)() | Alınacak metni alır veya ayarlar. |
| virtual [get_Type](../field/get_type/)() const | Microsoft Word alan türünü alır. |
| [GetFieldCode](../field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Alanı belgeden kaldırır. Alanın hemen sonrasındaki bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğuysa, üst paragrafını döndürür. Alan zaten kaldırılmışsa, **null** döndürür. |
| [set_IsDirty](../field/set_isdirty/)(bool) | [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) için ayarlayıcı. |
| [set_IsLocked](../field/set_islocked/)(bool) | [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) için ayarlayıcı. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) için ayarlayıcı. |
| [set_Result](../field/set_result/)(const System::String\&) | [Aspose::Words::Fields::Field::get_Result](../field/get_result/) için ayarlayıcı. |
| [set_Text](./set_text/)(const System::String\&) | [Aspose::Words::Fields::FieldShape::get_Text](./get_text/) için ayarlayıcı. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Alan bağlantısını kaldırır. |
| [Update](../field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
| [Update](../field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |

## Örnekler



BIDIOUTLINE alanlarıyla sağdan sola dillerle uyumlu listelerin nasıl oluşturulacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// BIDIOUTLINE alanı, AUTONUM/LISTNUM alanları gibi paragraflara numara verir,
// ancak sadece sağdan sola düzenleme dili etkin olduğunda, örneğin İbranice veya Arapça, görünür.
// Aşağıdaki alan ".1" görüntüleyecek, bu "1." liste numarasının sağdan sola eşdeğeridir.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldBidiOutline>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true));
builder->Writeln(u"שלום");

ASSERT_EQ(u" BIDIOUTLINE ", field->GetFieldCode());

// İki tane daha BIDIOUTLINE alanı ekleyin, bunlar ".2" ve ".3" görüntüleyecek.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");

// Belgedeki her paragraf için yatay metin hizalamasını sağdan sola (RTL) olarak ayarlayın.
for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)))
{
    para->get_ParagraphFormat()->set_Bidi(true);
}

// Microsoft Word'de sağdan sola bir düzenleme dili etkinleştirirsek, alanlarımız sayıları gösterecek.
// Aksi takdirde "###" görüntüleyecekler.
doc->Save(get_ArtifactsDir() + u"Field.BIDIOUTLINE.docx");
```


SHAPE ve EMBED gibi bazı eski Microsoft Word alanlarının yükleme sırasında nasıl işlendiğini gösterir.
```cpp
// Microsoft Word 2003'te oluşturulmuş bir belgeyi açın.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Legacy fields.doc");

// Word belgesini açıp Alt+F9 tuşlarına basarsak, bir SHAPE ve bir EMBED alanı göreceğiz.
// Bir SHAPE alanı, "In line with text" sarma stilinin etkin olduğu bir AutoShape nesnesi için çapa/tuval görevi görür.
// Bir EMBED alanı aynı işlevi görür, ancak gömülü bir nesne için,
// örneğin harici bir Excel belgesinden bir elektronik tablo.
// Ancak, bu alanlar belgenin Fields koleksiyonunda görünmez.
ASSERT_EQ(0, doc->get_Range()->get_Fields()->get_Count());

// Bu alanlar yalnızca eski Microsoft Word sürümlerinde desteklenir.
// Belge yükleme süreci bu alanları Shape nesnelerine dönüştürecek,
// ki bunlara belgenin düğüm koleksiyonunda erişebiliriz.
System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);
ASSERT_EQ(3, shapes->get_Count());

// İlk Shape düğümü, giriş belgesindeki SHAPE alanına karşılık gelir,
// bu da AutoShape için satır içi tuvaldir.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(0));
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Image, shape->get_ShapeType());

// İkinci Shape düğümü, AutoShape'in kendisidir.
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(1));
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Can, shape->get_ShapeType());

// Üçüncü Shape, harici elektronik tabloyu içeren EMBED alanıydı.
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(2));
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::OleObject, shape->get_ShapeType());
```

## Ayrıca Bakınız

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
