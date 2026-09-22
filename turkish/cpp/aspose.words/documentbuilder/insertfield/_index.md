---
title: "Aspose::Words::DocumentBuilder::InsertField metodu"
linktitle: "InsertField"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::InsertField metodu. Bir Word alanını belgeye ekler ve isteğe bağlı olarak C++'da alan sonucunu günceller."
type: docs
weight: 34000
url: /tr/cpp/aspose.words/documentbuilder/insertfield/
---
## DocumentBuilder::InsertField(Aspose::Words::Fields::FieldType, bool) method


Bir belgeye Word alanı ekler ve isteğe bağlı olarak alan sonucunu günceller.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(Aspose::Words::Fields::FieldType fieldType, bool updateField)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | Eklenecek alanın türü. |
| updateField | bool | Alanı hemen güncelleyip güncellemeyeceğini belirtir. |

### ReturnValue

Eklenen alanı temsil eden bir [Field](../../../aspose.words.fields/field/) nesnesi.
## Açıklamalar


Bu metod bir belgeye alan ekler. Aspose.Words çoğu türdeki alanları güncelleyebilir, ancak hepsini değil. Daha fazla ayrıntı için [InsertField()](../) aşırı yüklemesine bakın.

## Örnekler



FieldType kullanarak bir belgeye alan eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Oluşturucu alanları eklerken güncelleyip güncellemeyeceğini belirleyen bir bayrak geçirerek iki alan ekleyin.
// Bazı durumlarda, alanları güncellemek hesaplama açısından maliyetli olabilir ve güncellemeyi ertelemek iyi bir fikir olabilir.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
builder->Write(u"This document was written by ");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, updateInsertedFieldsImmediately);

builder->InsertParagraph();
builder->Write(u"\nThis is page ");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldPage, updateInsertedFieldsImmediately);

ASSERT_EQ(u" AUTHOR ", doc->get_Range()->get_Fields()->idx_get(0)->GetFieldCode());
ASSERT_EQ(u" PAGE ", doc->get_Range()->get_Fields()->idx_get(1)->GetFieldCode());

if (updateInsertedFieldsImmediately)
{
    ASSERT_EQ(u"John Doe", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
    ASSERT_EQ(u"1", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
}
else
{
    ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
    ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

    // Bu alanları güncelleme metodlarını kullanarak manuel olarak güncellememiz gerekecek.
    doc->get_Range()->get_Fields()->idx_get(0)->Update();

    ASSERT_EQ(u"John Doe", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

    doc->UpdateFields();

    ASSERT_EQ(u"1", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
}
```

## Ayrıca Bakınız

* Class [Field](../../../aspose.words.fields/field/)
* Enum [FieldType](../../../aspose.words.fields/fieldtype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertField(const System::String\&) method


Bir belgeye Word alanı ekler ve alan sonucunu günceller.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(const System::String &fieldCode)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fieldCode | const System::String\& | The field code to insert (without curly braces). |

### ReturnValue

Eklenen alanı temsil eden bir [Field](../../../aspose.words.fields/field/) nesnesi.
## Açıklamalar


Bu yöntem bir belgeye alan ekler ve alan sonucunu hemen günceller. Aspose.Words çoğu türdeki alanları güncelleyebilir, ancak hepsini değil. Daha fazla ayrıntı için [InsertField()](../) aşırı yüklemesine bakın.

## Örnekler



Alanların nasıl ekleneceğini ve belge oluşturucunun imlecinin onlara nasıl taşınacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertField(u"MERGEFIELD MyMergeField1 \\* MERGEFORMAT");
builder->InsertField(u"MERGEFIELD MyMergeField2 \\* MERGEFORMAT");

// İmleci ilk MERGEFIELD'e taşıyın.
builder->MoveToMergeField(u"MyMergeField1", true, false);

// İmlecin ilk MERGEFIELD'den hemen sonra ve ikincisinden önce konumlandırıldığını unutmayın.
ASPOSE_ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Start(), builder->get_CurrentNode());
ASPOSE_ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_End(), builder->get_CurrentNode()->get_PreviousSibling());

// Oluşturucu kullanarak alanın alan kodunu veya içeriğini düzenlemek istiyorsak,
// imlecinin bir alanın içinde olması gerekir.
// Bunu bir alanın içine yerleştirmek için belge oluşturucunun MoveTo metodunu çağırmamız gerekir
// ve alanın başlangıç ya da ayırıcı düğümünü argüman olarak geçirin.
builder->Write(u" Text between our merge fields. ");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.MergeFields.docx");
```


Bir alan kodu kullanarak bir belgeye alan eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// InsertField yönteminin bu aşırı yüklemesi, eklenen alanları otomatik olarak günceller.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```

## Ayrıca Bakınız

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertField(const System::String\&, const System::String\&) method


Bir belgeye Word alanı ekler ve alan sonucunu güncellemez.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(const System::String &fieldCode, const System::String &fieldValue)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fieldCode | const System::String\& | The field code to insert (without curly braces). |
| fieldValue | const System::String\& | Eklenecek alan değeri. Değeri olmayan alanlar için **null** geçirin. |

### ReturnValue

Eklenen alanı temsil eden bir [Field](../../../aspose.words.fields/field/) nesnesi.
## Açıklamalar


[Fields](../../../aspose.words.fields/) in Microsoft Word documents consist of a field code and a field result. The field code is like a formula and the field result is like the value that the formula produces. The field code may also contain field switches that are like additional instructions to perform a specific action.

Microsoft Word'de Alt+F9 kısayolunu kullanarak belge içinde alan kodlarını ve sonuçlarını görüntüleme arasında geçiş yapabilirsiniz. Alan kodları küme parantezleri ( { } ) arasında görünür.

Bir alan oluşturmak için alan türünü, alan kodunu ve bir "yer tutucu" alan değerini belirtmeniz gerekir. Belirli bir alan kodu sözdiziminden emin değilseniz, önce Microsoft Word'de alanı oluşturun ve kodunu görmek için geçiş yapın.

Aspose.Words çoğu alan türü için alan sonuçlarını hesaplayabilir, ancak bu yöntem alan sonucunu otomatik olarak güncellemez. Alan sonucu otomatik olarak hesaplanmadığı için, alan sonucuna eklenecek bir dize değeri (ya da boş bir dize) geçirmeniz beklenir. Bu değer, alan güncellenene kadar yer tutucu olarak alan sonucunda kalır. Alan sonucunu güncellemek için size döndürülen alan nesnesi üzerinde [Update](../../../aspose.words.fields/field/update/) metodunu çağırabilir veya tüm belgede alanları güncellemek için [UpdateFields](../../document/updatefields/) metodunu kullanabilirsiniz.

## Örnekler



Bir bölümde sayfa numaralandırmasını nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Section 1, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 3.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Writeln(u"Section 2, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 3.");

// Belge oluşturucuyu ilk bölümün birincil üstbilgi kısmına taşıyın,
// bu bölümdeki her sayfa bunu görüntüleyecek.
builder->MoveToSection(0);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);

// Bir PAGE alanı ekleyin, bu alan geçerli sayfanın numarasını gösterecektir.
builder->Write(u"Page ");
builder->InsertField(u"PAGE", u"");

// Bölümü, PAGE alanlarının gösterdiği sayfa sayısının 5'ten başlaması için yapılandırın.
// Ayrıca, tüm PAGE alanlarını sayfa numaralarını büyük harf Roma rakamlarıyla göstermeleri için yapılandırın.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageStartingNumber(5);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);

// İkinci bölüm için başka bir birincil üstbilgi oluşturun, içinde başka bir PAGE alanı olsun.
builder->MoveToSection(1);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->Write(u" - ");
builder->InsertField(u"PAGE", u"");
builder->Write(u" - ");

// Bölümü, PAGE alanlarının gösterdiği sayfa sayısının 10'dan başlaması için yapılandırın.
// Ayrıca, tüm PAGE alanlarını sayfa numaralarını Arap rakamlarıyla göstermeleri için yapılandırın.
pageSetup = doc->get_Sections()->idx_get(1)->get_PageSetup();
pageSetup->set_PageStartingNumber(10);
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::Arabic);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageNumbering.docx");
```

## Ayrıca Bakınız

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
