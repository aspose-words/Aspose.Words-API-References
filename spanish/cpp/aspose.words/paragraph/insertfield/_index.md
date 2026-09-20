---
title: "Aspose::Words::Paragraph::InsertField método"
linktitle: "InsertField"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Paragraph::InsertField método. Inserta un campo en este párrafo en C++."
type: docs
weight: 29000
url: /es/cpp/aspose.words/paragraph/insertfield/
---
## Paragraph::InsertField(Aspose::Words::Fields::FieldType, bool, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Inserta un campo en este párrafo.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(Aspose::Words::Fields::FieldType fieldType, bool updateField, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | El tipo del campo a insertar. |
| updateField | bool | Especifica si se debe actualizar el campo inmediatamente. |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Nodo de referencia dentro de este párrafo (si *refNode* es **null**, entonces se agrega al final del párrafo). |
| isAfter | bool | Si se debe insertar el campo después o antes del nodo de referencia. |

### ReturnValue

Un objeto [Field](../../../aspose.words.fields/field/) que representa el campo insertado.

## Ejemplos



Muestra varias formas de agregar campos a un párrafo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// A continuación hay tres formas de insertar un campo en un párrafo.
// 1 -  Inserta un campo AUTHOR en un párrafo después de uno de los nodos hijos del párrafo:
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 -  Inserta un campo QUOTE después de uno de los nodos hijos del párrafo:
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  Inserta un campo QUOTE antes de uno de los nodos hijos del párrafo,
// y haz que muestre un valor de marcador de posición:
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// Este campo mostrará su valor de marcador de posición hasta que lo actualicemos.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## Ver también

* Class [Field](../../../aspose.words.fields/field/)
* Enum [FieldType](../../../aspose.words.fields/fieldtype/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::InsertField(const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Inserta un campo en este párrafo.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(const System::String &fieldCode, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fieldCode | const System::String\& | El código de campo a insertar (sin llaves). |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Nodo de referencia dentro de este párrafo (si *refNode* es **null**, entonces se agrega al final del párrafo). |
| isAfter | bool | Si se debe insertar el campo después o antes del nodo de referencia. |

### ReturnValue

Un objeto [Field](../../../aspose.words.fields/field/) que representa el campo insertado.

## Ejemplos



Muestra varias formas de agregar campos a un párrafo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// A continuación hay tres formas de insertar un campo en un párrafo.
// 1 -  Inserta un campo AUTHOR en un párrafo después de uno de los nodos hijos del párrafo:
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 -  Inserta un campo QUOTE después de uno de los nodos hijos del párrafo:
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  Inserta un campo QUOTE antes de uno de los nodos hijos del párrafo,
// y haz que muestre un valor de marcador de posición:
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// Este campo mostrará su valor de marcador de posición hasta que lo actualicemos.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## Ver también

* Class [Field](../../../aspose.words.fields/field/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::InsertField(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Inserta un campo en este párrafo.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(const System::String &fieldCode, const System::String &fieldValue, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fieldCode | const System::String\& | El código de campo a insertar (sin llaves). |
| fieldValue | const System::String\& | El valor del campo a insertar. Pase **null** para los campos que no tienen un valor. |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Nodo de referencia dentro de este párrafo (si *refNode* es **null**, entonces se agrega al final del párrafo). |
| isAfter | bool | Si se debe insertar el campo después o antes del nodo de referencia. |

### ReturnValue

Un objeto [Field](../../../aspose.words.fields/field/) que representa el campo insertado.

## Ejemplos



Muestra varias formas de agregar campos a un párrafo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// A continuación hay tres formas de insertar un campo en un párrafo.
// 1 -  Inserta un campo AUTHOR en un párrafo después de uno de los nodos hijos del párrafo:
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 -  Inserta un campo QUOTE después de uno de los nodos hijos del párrafo:
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  Inserta un campo QUOTE antes de uno de los nodos hijos del párrafo,
// y haz que muestre un valor de marcador de posición:
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// Este campo mostrará su valor de marcador de posición hasta que lo actualicemos.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## Ver también

* Class [Field](../../../aspose.words.fields/field/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
