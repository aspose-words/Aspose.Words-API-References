---
title: "Aspose::Words::Paragraph::InsertField метод"
linktitle: "InsertField"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Paragraph::InsertField метод. Вставляет поле в этот абзац в C++."
type: docs
weight: 29000
url: /ru/cpp/aspose.words/paragraph/insertfield/
---
## Paragraph::InsertField(Aspose::Words::Fields::FieldType, bool, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Вставляет поле в этот абзац.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(Aspose::Words::Fields::FieldType fieldType, bool updateField, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | Тип поля для вставки. |
| updateField | bool | Указывает, следует ли обновлять поле немедленно. |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Ссылка‑узел внутри этого абзаца (если *refNode* **null**, то добавляется в конец абзаца). |
| isAfter | bool | Нужно ли вставлять поле после или перед ссылкой‑узлом. |

### ReturnValue

Объект [Field](../../../aspose.words.fields/field/), представляющий вставленное поле.

## Примеры



Показывает различные способы добавления полей в абзац.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Ниже представлены три способа вставки поля в абзац.
// 1 -  Вставьте поле AUTHOR в абзац после одного из дочерних узлов абзаца:
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 -  Вставьте поле QUOTE после одного из дочерних узлов абзаца:
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  Вставьте поле QUOTE перед одним из дочерних узлов абзаца,
// и заставьте его отображать значение‑заполнитель:
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// Это поле будет отображать своё значение‑заполнитель, пока мы не обновим его.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## См. также

* Class [Field](../../../aspose.words.fields/field/)
* Enum [FieldType](../../../aspose.words.fields/fieldtype/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::InsertField(const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Вставляет поле в этот абзац.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(const System::String &fieldCode, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldCode | const System::String\& | Код поля для вставки (без фигурных скобок). |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Ссылка‑узел внутри этого абзаца (если *refNode* **null**, то добавляется в конец абзаца). |
| isAfter | bool | Нужно ли вставлять поле после или перед ссылкой‑узлом. |

### ReturnValue

Объект [Field](../../../aspose.words.fields/field/), представляющий вставленное поле.

## Примеры



Показывает различные способы добавления полей в абзац.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Ниже представлены три способа вставки поля в абзац.
// 1 -  Вставьте поле AUTHOR в абзац после одного из дочерних узлов абзаца:
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 -  Вставьте поле QUOTE после одного из дочерних узлов абзаца:
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  Вставьте поле QUOTE перед одним из дочерних узлов абзаца,
// и заставьте его отображать значение‑заполнитель:
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// Это поле будет отображать своё значение‑заполнитель, пока мы не обновим его.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## См. также

* Class [Field](../../../aspose.words.fields/field/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::InsertField(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Вставляет поле в этот абзац.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(const System::String &fieldCode, const System::String &fieldValue, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldCode | const System::String\& | Код поля для вставки (без фигурных скобок). |
| fieldValue | const System::String\& | Значение поля для вставки. Передайте **null** для полей, у которых нет значения. |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Ссылка‑узел внутри этого абзаца (если *refNode* **null**, то добавляется в конец абзаца). |
| isAfter | bool | Нужно ли вставлять поле после или перед ссылкой‑узлом. |

### ReturnValue

Объект [Field](../../../aspose.words.fields/field/), представляющий вставленное поле.

## Примеры



Показывает различные способы добавления полей в абзац.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Ниже представлены три способа вставки поля в абзац.
// 1 -  Вставьте поле AUTHOR в абзац после одного из дочерних узлов абзаца:
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 -  Вставьте поле QUOTE после одного из дочерних узлов абзаца:
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  Вставьте поле QUOTE перед одним из дочерних узлов абзаца,
// и заставьте его отображать значение‑заполнитель:
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// Это поле будет отображать своё значение‑заполнитель, пока мы не обновим его.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## См. также

* Class [Field](../../../aspose.words.fields/field/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
