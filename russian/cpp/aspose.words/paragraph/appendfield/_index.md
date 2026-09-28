---
title: "Aspose::Words::Paragraph::AppendField method"
linktitle: "AppendField"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Paragraph::AppendField method. Добавляет поле в этот абзац в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words/paragraph/appendfield/
---
## Paragraph::AppendField(Aspose::Words::Fields::FieldType, bool) method


Добавляет поле к этому абзацу.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(Aspose::Words::Fields::FieldType fieldType, bool updateField)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | Тип поля для добавления. |
| updateField | bool | Указывает, следует ли обновлять поле немедленно. |

### ReturnValue

Объект [Field](../../../aspose.words.fields/field/), представляющий добавленное поле.

## Примеры



Показывает различные способы добавления полей в абзац.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Ниже представлены три способа добавить поле в конец абзаца.
// 1 -  Добавьте поле DATE, используя тип поля, а затем обновите его:
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  Добавьте поле TIME, используя код поля:
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  Добавьте поле QUOTE, используя код поля, и заставьте его отображать значение-заполнитель:
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// Это поле будет отображать своё значение‑заполнитель, пока мы не обновим его.
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## См. также

* Class [Field](../../../aspose.words.fields/field/)
* Enum [FieldType](../../../aspose.words.fields/fieldtype/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::AppendField(const System::String\&) method


Добавляет поле к этому абзацу.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(const System::String &fieldCode)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldCode | const System::String\& | Код поля для добавления (без фигурных скобок). |

### ReturnValue

Объект [Field](../../../aspose.words.fields/field/), представляющий добавленное поле.

## Примеры



Показывает различные способы добавления полей в абзац.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Ниже представлены три способа добавить поле в конец абзаца.
// 1 -  Добавьте поле DATE, используя тип поля, а затем обновите его:
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  Добавьте поле TIME, используя код поля:
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  Добавьте поле QUOTE, используя код поля, и заставьте его отображать значение-заполнитель:
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// Это поле будет отображать своё значение‑заполнитель, пока мы не обновим его.
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## См. также

* Class [Field](../../../aspose.words.fields/field/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::AppendField(const System::String\&, const System::String\&) method


Добавляет поле к этому абзацу.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(const System::String &fieldCode, const System::String &fieldValue)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldCode | const System::String\& | Код поля для добавления (без фигурных скобок). |
| fieldValue | const System::String\& | Значение поля для добавления. Передайте **null** для полей, у которых нет значения. |

### ReturnValue

Объект [Field](../../../aspose.words.fields/field/), представляющий добавленное поле.

## Примеры



Показывает различные способы добавления полей в абзац.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Ниже представлены три способа добавить поле в конец абзаца.
// 1 -  Добавьте поле DATE, используя тип поля, а затем обновите его:
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  Добавьте поле TIME, используя код поля:
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  Добавьте поле QUOTE, используя код поля, и заставьте его отображать значение-заполнитель:
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// Это поле будет отображать своё значение‑заполнитель, пока мы не обновим его.
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## См. также

* Class [Field](../../../aspose.words.fields/field/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
