---
title: "Método Aspose::Words::Paragraph::AppendField"
linktitle: "AppendField"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Paragraph::AppendField. Añade un campo a este párrafo en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words/paragraph/appendfield/
---
## Paragraph::AppendField(Aspose::Words::Fields::FieldType, bool) method


Añade un campo a este párrafo.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(Aspose::Words::Fields::FieldType fieldType, bool updateField)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | El tipo del campo a añadir. |
| updateField | bool | Especifica si se debe actualizar el campo inmediatamente. |

### ReturnValue

Un objeto [Field](../../../aspose.words.fields/field/) que representa el campo añadido.

## Ejemplos



Muestra varias formas de añadir campos a un párrafo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// A continuación se presentan tres formas de añadir un campo al final de un párrafo.
// 1 -  Añade un campo DATE usando un tipo de campo, y luego actualízalo:
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  Añade un campo TIME usando un código de campo:
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  Añade un campo QUOTE usando un código de campo, y haz que muestre un valor de marcador de posición:
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// Este campo mostrará su valor de marcador de posición hasta que lo actualicemos.
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## Ver también

* Class [Field](../../../aspose.words.fields/field/)
* Enum [FieldType](../../../aspose.words.fields/fieldtype/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::AppendField(const System::String\&) method


Añade un campo a este párrafo.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(const System::String &fieldCode)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fieldCode | const System::String\& | El código de campo a añadir (sin llaves). |

### ReturnValue

Un objeto [Field](../../../aspose.words.fields/field/) que representa el campo añadido.

## Ejemplos



Muestra varias formas de añadir campos a un párrafo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// A continuación se presentan tres formas de añadir un campo al final de un párrafo.
// 1 -  Añade un campo DATE usando un tipo de campo, y luego actualízalo:
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  Añade un campo TIME usando un código de campo:
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  Añade un campo QUOTE usando un código de campo, y haz que muestre un valor de marcador de posición:
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// Este campo mostrará su valor de marcador de posición hasta que lo actualicemos.
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## Ver también

* Class [Field](../../../aspose.words.fields/field/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::AppendField(const System::String\&, const System::String\&) method


Añade un campo a este párrafo.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(const System::String &fieldCode, const System::String &fieldValue)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fieldCode | const System::String\& | El código de campo a añadir (sin llaves). |
| fieldValue | const System::String\& | El valor del campo a añadir. Pasa **null** para los campos que no tienen un valor. |

### ReturnValue

Un objeto [Field](../../../aspose.words.fields/field/) que representa el campo añadido.

## Ejemplos



Muestra varias formas de añadir campos a un párrafo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// A continuación se presentan tres formas de añadir un campo al final de un párrafo.
// 1 -  Añade un campo DATE usando un tipo de campo, y luego actualízalo:
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  Añade un campo TIME usando un código de campo:
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  Añade un campo QUOTE usando un código de campo, y haz que muestre un valor de marcador de posición:
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// Este campo mostrará su valor de marcador de posición hasta que lo actualicemos.
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## Ver también

* Class [Field](../../../aspose.words.fields/field/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
