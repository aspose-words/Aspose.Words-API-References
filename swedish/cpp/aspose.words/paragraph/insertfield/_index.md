---
title: "Aspose::Words::Paragraph::InsertField‑metod"
linktitle: "InsertField"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Paragraph::InsertField‑metod. Infogar ett fält i detta stycke i C++."
type: docs
weight: 29000
url: /sv/cpp/aspose.words/paragraph/insertfield/
---
## Paragraph::InsertField(Aspose::Words::Fields::FieldType, bool, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Infogar ett fält i detta stycke.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(Aspose::Words::Fields::FieldType fieldType, bool updateField, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | Typen av fältet som ska infogas. |
| updateField | bool | Anger om fältet ska uppdateras omedelbart. |
| refNode | const System::SharedPtr\\<Aspose::Words::Node\\>\\& | Referensnod inom detta stycke (om *refNode* är **null**, läggs den till i slutet av stycket). |
| isAfter | bool | Om fältet ska infogas efter eller före referensnoden. |

### ReturnValue

Ett [Field](../../../aspose.words.fields/field/)‑objekt som representerar det infogade fältet.

## Exempel



Visar olika sätt att lägga till fält i ett stycke.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Nedan följer tre sätt att infoga ett fält i ett stycke.
// 1 -  Infoga ett AUTHOR‑fält i ett stycke efter en av styckets barnnoder:
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 -  Infoga ett QUOTE‑fält efter en av styckets barnnoder:
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  Infoga ett QUOTE‑fält före en av styckets barnnoder,
// och få det att visa ett platshållarvärde:
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// Detta fält kommer att visa sitt platshållarvärde tills vi uppdaterar det.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## Se även

* Class [Field](../../../aspose.words.fields/field/)
* Enum [FieldType](../../../aspose.words.fields/fieldtype/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::InsertField(const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Infogar ett fält i detta stycke.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(const System::String &fieldCode, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldCode | const System::String\& | Fältkoden att infoga (utan måsvingar). |
| refNode | const System::SharedPtr\\<Aspose::Words::Node\\>\\& | Referensnod inom detta stycke (om *refNode* är **null**, läggs den till i slutet av stycket). |
| isAfter | bool | Om fältet ska infogas efter eller före referensnoden. |

### ReturnValue

Ett [Field](../../../aspose.words.fields/field/)‑objekt som representerar det infogade fältet.

## Exempel



Visar olika sätt att lägga till fält i ett stycke.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Nedan följer tre sätt att infoga ett fält i ett stycke.
// 1 -  Infoga ett AUTHOR‑fält i ett stycke efter en av styckets barnnoder:
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 -  Infoga ett QUOTE‑fält efter en av styckets barnnoder:
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  Infoga ett QUOTE‑fält före en av styckets barnnoder,
// och få det att visa ett platshållarvärde:
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// Detta fält kommer att visa sitt platshållarvärde tills vi uppdaterar det.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## Se även

* Class [Field](../../../aspose.words.fields/field/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::InsertField(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Infogar ett fält i detta stycke.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(const System::String &fieldCode, const System::String &fieldValue, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldCode | const System::String\& | Fältkoden att infoga (utan måsvingar). |
| fieldValue | const System::String\& | Fältvärdet att infoga. Skicka **null** för fält som inte har något värde. |
| refNode | const System::SharedPtr\\<Aspose::Words::Node\\>\\& | Referensnod inom detta stycke (om *refNode* är **null**, läggs den till i slutet av stycket). |
| isAfter | bool | Om fältet ska infogas efter eller före referensnoden. |

### ReturnValue

Ett [Field](../../../aspose.words.fields/field/)‑objekt som representerar det infogade fältet.

## Exempel



Visar olika sätt att lägga till fält i ett stycke.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Nedan följer tre sätt att infoga ett fält i ett stycke.
// 1 -  Infoga ett AUTHOR‑fält i ett stycke efter en av styckets barnnoder:
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 -  Infoga ett QUOTE‑fält efter en av styckets barnnoder:
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  Infoga ett QUOTE‑fält före en av styckets barnnoder,
// och få det att visa ett platshållarvärde:
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// Detta fält kommer att visa sitt platshållarvärde tills vi uppdaterar det.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## Se även

* Class [Field](../../../aspose.words.fields/field/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
