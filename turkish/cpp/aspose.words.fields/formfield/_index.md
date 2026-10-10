---
title: "Aspose::Words::Fields::FormField class"
linktitle: "FormField"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FormField sınıfı. Tek bir form alanını temsil eder. Daha fazla bilgi edinmek için C++ belgeleri makalesini ziyaret edin."
type: docs
weight: 112000
url: /tr/cpp/aspose.words.fields/formfield/
---
## FormField class


Tek bir form alanını temsil eder. Daha fazla bilgi edinmek için [Working with Form Fields](https://docs.aspose.com/words/cpp/working-with-form-fields/) dokümantasyon makalesini ziyaret edin.

```cpp
class FormField : public Aspose::Words::SpecialChar
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Bir ziyaretçiyi kabul eder. |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [get_CalculateOnExit](./get_calculateonexit/)() | Doğru, belirtilen form alanına referanslar alan terk edildiğinde otomatik olarak güncelleniyorsa. |
| [get_CheckBoxSize](./get_checkboxsize/)() | Onay kutusunun boyutunu puan cinsinden alır veya ayarlar. Yalnızca [IsCheckBoxExactSize](./get_ischeckboxexactsize/) **true** olduğunda etkili olur. |
| [get_Checked](./get_checked/)() | Onay kutusu form alanının işaretli durumunu alır veya ayarlar. Bu özelliğin varsayılan değeri **false**. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Özel düğüm tanımlayıcısını belirtir. |
| [get_Default](./get_default/)() | Onay kutusu form alanının varsayılan değerini alır veya ayarlar. Bu özelliğin varsayılan değeri **false**. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Bu düğümün ait olduğu belgeyi alır. |
| [get_DropDownItems](./get_dropdownitems/)() | Açılır menü form alanının öğelerine erişim sağlar. |
| [get_DropDownSelectedIndex](./get_dropdownselectedindex/)() | Açılır menü form alanında şu anda seçili öğeyi belirten dizini alır. |
| [get_Enabled](./get_enabled/)() | Form alanı etkinse doğru. |
| [get_EntryMacro](./get_entrymacro/)() | Form alanı için giriş makro adını döndürür veya ayarlar. |
| [get_ExitMacro](./get_exitmacro/)() | Form alanı için çıkış makro adını döndürür veya ayarlar. |
| [get_Font](../../aspose.words/inline/get_font/)() | Bu nesnenin yazı tipi biçimlendirmesine erişim sağlar. |
| [get_HelpText](./get_helptext/)() | Form alanı odakta iken ve kullanıcı F1 tuşuna bastığında mesaj kutusunda gösterilen metni döndürür veya ayarlar. |
| [get_IsCheckBoxExactSize](./get_ischeckboxexactsize/)() | Metin kutusunun boyutunun otomatik mi yoksa açıkça belirtilmiş mi olduğunu gösteren boolean değeri alır veya ayarlar. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | Bu düğüm diğer düğümleri içerebiliyorsa **true** döndürür. |
| [get_IsDeleteRevision](../../aspose.words/inline/get_isdeleterevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de silinmişse true döndürür. |
| [get_IsFormatRevision](../../aspose.words/inline/get_isformatrevision/)() | Değişiklik izleme etkinleştirildiği sırada Microsoft Word'de nesnenin biçimlendirmesi değiştirildiyse true döndürür. |
| [get_IsInsertRevision](../../aspose.words/inline/get_isinsertrevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de eklenmişse true döndürür. |
| [get_IsMoveFromRevision](../../aspose.words/inline/get_ismovefromrevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de taşınmış (silinmiş) ise **true** döndürür. |
| [get_IsMoveToRevision](../../aspose.words/inline/get_ismovetorevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de taşınmış (eklenmiş) ise **true** döndürür. |
| [get_MaxLength](./get_maxlength/)() | Metin alanı için maksimum uzunluk. Uzunluk sınırlı değilse sıfır. |
| [get_Name](./get_name/)() | Form alanı adını alır veya ayarlar. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Bu düğümü hemen izleyen düğümü alır. |
| [get_NodeType](./get_nodetype/)() const override | Döndürür [FormField](../../aspose.words/nodetype/). |
| [get_OwnHelp](./get_ownhelp/)() | Form alanı odakta iken ve kullanıcı F1 tuşuna bastığında mesaj kutusunda gösterilen metnin kaynağını belirtir. |
| [get_OwnStatus](./get_ownstatus/)() | Form alanı odakta iken durum çubuğunda gösterilen metnin kaynağını belirtir. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Bu düğümün doğrudan ebeveynini alır. |
| [get_ParentParagraph](../../aspose.words/inline/get_parentparagraph/)() | Bu düğümün üst [Paragraph](../../aspose.words/paragraph/) öğesini alır. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Bu düğümden hemen önce gelen düğümü alır. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Bu düğümde bulunan belge bölümünü temsil eden bir [Range](../../aspose.words/range/) nesnesi döndürür. |
| [get_Result](./get_result/)() | Bu form alanının sonucunu temsil eden bir dizeyi alır veya ayarlar. |
| [get_StatusText](./get_statustext/)() | Form alanı odakta iken durum çubuğunda gösterilen metni döndürür veya ayarlar. |
| [get_TextInputDefault](./get_textinputdefault/)() | Metin form alanının varsayılan dizesini veya bir hesaplama ifadesini alır veya ayarlar. |
| [get_TextInputFormat](./get_textinputformat/)() | Metin form alanı için metin biçimlendirmesini döndürür veya ayarlar. |
| [get_TextInputType](./get_textinputtype/)() | Metin form alanının türünü alır. |
| [get_Type](./get_type/)() | Form alanı türünü döndürür. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Belirtilen [NodeType](../../aspose.words/nodetype/) ilk atasını alır. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetText](../../aspose.words/specialchar/gettext/)() override | Bu düğümün temsil ettiği özel karakteri alır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre bir sonraki düğümü alır. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Bir düğüm türü enum değerini kullanıcı dostu bir dizeye dönüştüren yardımcı bir yöntem. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendisini üst düğümden kaldırır. |
| [RemoveField](./removefield/)() | Form alanının özel karakteri değil, tamamını kaldırır. |
| [set_CalculateOnExit](./set_calculateonexit/)(bool) | [Aspose::Words::Fields::FormField::get_CalculateOnExit](./get_calculateonexit/) için ayarlayıcı. |
| [set_CheckBoxSize](./set_checkboxsize/)(double) | [Aspose::Words::Fields::FormField::get_CheckBoxSize](./get_checkboxsize/) için ayarlayıcı. |
| [set_Checked](./set_checked/)(bool) | [Aspose::Words::Fields::FormField::get_Checked](./get_checked/) için ayarlayıcı. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/) için ayarlayıcı. |
| [set_Default](./set_default/)(bool) | [Aspose::Words::Fields::FormField::get_Default](./get_default/) için ayarlayıcı. |
| [set_DropDownSelectedIndex](./set_dropdownselectedindex/)(int32_t) | Açılır menü form alanında şu anda seçili öğeyi belirten dizini ayarlar. |
| [set_Enabled](./set_enabled/)(bool) | Form alanı etkinse doğru. |
| [set_EntryMacro](./set_entrymacro/)(const System::String\&) | [Aspose::Words::Fields::FormField::get_EntryMacro](./get_entrymacro/) için ayarlayıcı. |
| [set_ExitMacro](./set_exitmacro/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FormField::get_ExitMacro](./get_exitmacro/). |
| [set_HelpText](./set_helptext/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FormField::get_HelpText](./get_helptext/). |
| [set_IsCheckBoxExactSize](./set_ischeckboxexactsize/)(bool) | Ayarlayıcı [Aspose::Words::Fields::FormField::get_IsCheckBoxExactSize](./get_ischeckboxexactsize/). |
| [set_MaxLength](./set_maxlength/)(int32_t) | Metin alanı için maksimum uzunluk. Uzunluk sınırlı değilse sıfır. |
| [set_Name](./set_name/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FormField::get_Name](./get_name/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_OwnHelp](./set_ownhelp/)(bool) | Ayarlayıcı [Aspose::Words::Fields::FormField::get_OwnHelp](./get_ownhelp/). |
| [set_OwnStatus](./set_ownstatus/)(bool) | Ayarlayıcı [Aspose::Words::Fields::FormField::get_OwnStatus](./get_ownstatus/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Result](./set_result/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FormField::get_Result](./get_result/). |
| [set_StatusText](./set_statustext/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FormField::get_StatusText](./get_statustext/). |
| [set_TextInputDefault](./set_textinputdefault/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FormField::get_TextInputDefault](./get_textinputdefault/). |
| [set_TextInputFormat](./set_textinputformat/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FormField::get_TextInputFormat](./get_textinputformat/). |
| [set_TextInputType](./set_textinputtype/)(Aspose::Words::Fields::TextFormFieldType) | Metin form alanının türünü ayarlar. |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTextInputValue](./settextinputvalue/)(const System::SharedPtr\<System::Object\>\&) | Metin biçimini [TextInputFormat](./get_textinputformat/) içinde belirtilen şekilde uygular ve değeri [Result](./get_result/) içinde depolar. |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye dışa aktarır. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Düğümün içeriğini belirtilen kaydetme seçeneklerini kullanarak bir dizeye dışa aktarır. |
| static [Type](./type/)() |  |
## Açıklamalar


Microsoft Word aşağıdaki form alanlarını sağlar: onay kutusu, metin girişi ve açılır liste (combobox).

[FormField](./) is an inline-node and can only be a child of [Paragraph](../../aspose.words/paragraph/).

[FormField](./) is represented in a document by a special character and positioned as a character within a line of text.

Word belgesindeki tam bir form alanı, birden fazla düğüm tarafından temsil edilen karmaşık bir yapıdır: alan başlangıcı, FORMTEXT gibi alan kodu, form alanı verisi, alan ayırıcı, alan sonucu, alan sonu ve bir yer imi. Bir Word belgesinde programlı olarak form alanları oluşturmak için [InsertCheckBox()](../), [InsertTextInput()](../) ve [InsertComboBox()](../) kullanın; bu yöntemler tüm form alanı düğümlerinin doğru sırada ve uygun durumda oluşturulmasını sağlar.

## Örnekler



Bir combo kutusunun nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please select a fruit: ");

// Kullanıcının bir dizi dizeden bir seçenek seçmesine izin veren bir combo kutusu ekleyin.
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"}), 0);

ASSERT_EQ(u"MyComboBox", comboBox->get_Name());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldFormDropDown, comboBox->get_Type());
ASSERT_EQ(u"Apple", comboBox->get_Result());

// Form alanı, bir "select" HTML etiketi şeklinde görünecek.
doc->Save(get_ArtifactsDir() + u"FormFields.Create.html");
```


Tüm [FormField](./) öğesinin, alan değerini de içerecek şekilde nasıl biçimlendirileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Form fields.docx");

System::SharedPtr<Aspose::Words::Fields::FormField> formField = doc->get_Range()->get_FormFields()->idx_get(0);
formField->get_Font()->set_Bold(true);
formField->get_Font()->set_Size(24);
formField->get_Font()->set_Color(System::Drawing::Color::get_Red());

formField->set_Result(u"Aspose.FormField");

doc = Aspose::Words::ApiExamples::DocumentHelper::SaveOpen(doc);

System::SharedPtr<Aspose::Words::Run> formFieldRun = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(1);

ASSERT_EQ(u"Aspose.FormField", formFieldRun->get_Text());
ASPOSE_ASSERT_EQ(true, formFieldRun->get_Font()->get_Bold());
ASPOSE_ASSERT_EQ(24, formFieldRun->get_Font()->get_Size());
ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), formFieldRun->get_Font()->get_Color().ToArgb());
```

## Ayrıca Bakınız

* Class [SpecialChar](../../aspose.words/specialchar/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
