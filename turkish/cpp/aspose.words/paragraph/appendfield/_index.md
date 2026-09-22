---
title: "Aspose::Words::Paragraph::AppendField yöntemi"
linktitle: "AppendField"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Paragraph::AppendField yöntemi. Bu paragrafın sonuna C++'ta bir alan ekler."
type: docs
weight: 4000
url: /tr/cpp/aspose.words/paragraph/appendfield/
---
## Paragraph::AppendField(Aspose::Words::Fields::FieldType, bool) method


Bu paragrafa bir alan ekler.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(Aspose::Words::Fields::FieldType fieldType, bool updateField)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | Eklenecek alanın türü. |
| updateField | bool | Alanı hemen güncelleyip güncellemeyeceğini belirtir. |

### ReturnValue

Eklenen alanı temsil eden bir [Field](../../../aspose.words.fields/field/) nesnesi.

## Örnekler



Bir paragrafa alan eklemenin çeşitli yollarını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Aşağıda bir paragrafın sonuna alan eklemenin üç yolu verilmiştir.
// 1 -  Bir alan türü kullanarak DATE alanı ekleyin ve ardından güncelleyin:
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  Bir alan kodu kullanarak TIME alanı ekleyin:
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  Bir alan kodu kullanarak QUOTE alanı ekleyin ve yer tutucu bir değer göstermesini sağlayın:
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// Bu alan, güncelleyin kadar yer tutucu değerini gösterecek.
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## Ayrıca Bakınız

* Class [Field](../../../aspose.words.fields/field/)
* Enum [FieldType](../../../aspose.words.fields/fieldtype/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::AppendField(const System::String\&) method


Bu paragrafa bir alan ekler.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(const System::String &fieldCode)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fieldCode | const System::String\& | Eklemek için alan kodu (küme parantezleri olmadan). |

### ReturnValue

Eklenen alanı temsil eden bir [Field](../../../aspose.words.fields/field/) nesnesi.

## Örnekler



Bir paragrafa alan eklemenin çeşitli yollarını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Aşağıda bir paragrafın sonuna alan eklemenin üç yolu verilmiştir.
// 1 -  Bir alan türü kullanarak DATE alanı ekleyin ve ardından güncelleyin:
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  Bir alan kodu kullanarak TIME alanı ekleyin:
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  Bir alan kodu kullanarak QUOTE alanı ekleyin ve yer tutucu bir değer göstermesini sağlayın:
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// Bu alan, güncelleyin kadar yer tutucu değerini gösterecek.
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## Ayrıca Bakınız

* Class [Field](../../../aspose.words.fields/field/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::AppendField(const System::String\&, const System::String\&) method


Bu paragrafa bir alan ekler.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(const System::String &fieldCode, const System::String &fieldValue)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fieldCode | const System::String\& | Eklemek için alan kodu (küme parantezleri olmadan). |
| fieldValue | const System::String\& | Eklemek için alan değeri. Değeri olmayan alanlar için **null** geçirin. |

### ReturnValue

Eklenen alanı temsil eden bir [Field](../../../aspose.words.fields/field/) nesnesi.

## Örnekler



Bir paragrafa alan eklemenin çeşitli yollarını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Aşağıda bir paragrafın sonuna alan eklemenin üç yolu verilmiştir.
// 1 -  Bir alan türü kullanarak DATE alanı ekleyin ve ardından güncelleyin:
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  Bir alan kodu kullanarak TIME alanı ekleyin:
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  Bir alan kodu kullanarak QUOTE alanı ekleyin ve yer tutucu bir değer göstermesini sağlayın:
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// Bu alan, güncelleyin kadar yer tutucu değerini gösterecek.
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## Ayrıca Bakınız

* Class [Field](../../../aspose.words.fields/field/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
