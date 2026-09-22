---
title: "Aspose::Words::Paragraph::InsertField metodu"
linktitle: "InsertField"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Paragraph::InsertField metodu. Bu paragrafta bir alan ekler C++'ta."
type: docs
weight: 29000
url: /tr/cpp/aspose.words/paragraph/insertfield/
---
## Paragraph::InsertField(Aspose::Words::Fields::FieldType, bool, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Bu paragrafa bir alan ekler.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(Aspose::Words::Fields::FieldType fieldType, bool updateField, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | Eklenecek alanın türü. |
| updateField | bool | Alanı hemen güncelleyip güncellemeyeceğini belirtir. |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Bu paragraftaki referans düğüm (eğer *refNode* **null** ise, paragrafın sonuna ekler). |
| isAfter | bool | Alanı referans düğümden önce mi yoksa sonra mı ekleyeceğiniz. |

### ReturnValue

Eklenen alanı temsil eden bir [Field](../../../aspose.words.fields/field/) nesnesi.

## Örnekler



Bir paragrafta alan eklemenin çeşitli yollarını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Aşağıda bir paragrafta alan eklemenin üç yolu verilmiştir.
// 1 -  Bir paragrafta, paragrafın bir alt düğümünden sonra bir AUTHOR alanı ekleyin:
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 -  Bir paragrafta, paragrafın bir alt düğümünden sonra bir QUOTE alanı ekleyin:
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  Bir paragrafta, paragrafın bir alt düğümünden önce bir QUOTE alanı ekleyin,
// ve yer tutucu bir değer göstermesini sağlayın:
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// Bu alan, güncelleyin kadar yer tutucu değerini gösterecek.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## Ayrıca Bakınız

* Class [Field](../../../aspose.words.fields/field/)
* Enum [FieldType](../../../aspose.words.fields/fieldtype/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::InsertField(const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Bu paragrafa bir alan ekler.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(const System::String &fieldCode, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fieldCode | const System::String\& | The field code to insert (without curly braces). |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Bu paragraftaki referans düğüm (eğer *refNode* **null** ise, paragrafın sonuna ekler). |
| isAfter | bool | Alanı referans düğümden önce mi yoksa sonra mı ekleyeceğiniz. |

### ReturnValue

Eklenen alanı temsil eden bir [Field](../../../aspose.words.fields/field/) nesnesi.

## Örnekler



Bir paragrafta alan eklemenin çeşitli yollarını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Aşağıda bir paragrafta alan eklemenin üç yolu verilmiştir.
// 1 -  Bir paragrafta, paragrafın bir alt düğümünden sonra bir AUTHOR alanı ekleyin:
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 -  Bir paragrafta, paragrafın bir alt düğümünden sonra bir QUOTE alanı ekleyin:
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  Bir paragrafta, paragrafın bir alt düğümünden önce bir QUOTE alanı ekleyin,
// ve yer tutucu bir değer göstermesini sağlayın:
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// Bu alan, güncelleyin kadar yer tutucu değerini gösterecek.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## Ayrıca Bakınız

* Class [Field](../../../aspose.words.fields/field/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::InsertField(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Bu paragrafa bir alan ekler.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(const System::String &fieldCode, const System::String &fieldValue, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fieldCode | const System::String\& | The field code to insert (without curly braces). |
| fieldValue | const System::String\& | Eklenecek alan değeri. Değeri olmayan alanlar için **null** geçirin. |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Bu paragraftaki referans düğüm (eğer *refNode* **null** ise, paragrafın sonuna ekler). |
| isAfter | bool | Alanı referans düğümden önce mi yoksa sonra mı ekleyeceğiniz. |

### ReturnValue

Eklenen alanı temsil eden bir [Field](../../../aspose.words.fields/field/) nesnesi.

## Örnekler



Bir paragrafta alan eklemenin çeşitli yollarını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Aşağıda bir paragrafta alan eklemenin üç yolu verilmiştir.
// 1 -  Bir paragrafta, paragrafın bir alt düğümünden sonra bir AUTHOR alanı ekleyin:
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 -  Bir paragrafta, paragrafın bir alt düğümünden sonra bir QUOTE alanı ekleyin:
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  Bir paragrafta, paragrafın bir alt düğümünden önce bir QUOTE alanı ekleyin,
// ve yer tutucu bir değer göstermesini sağlayın:
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// Bu alan, güncelleyin kadar yer tutucu değerini gösterecek.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## Ayrıca Bakınız

* Class [Field](../../../aspose.words.fields/field/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
