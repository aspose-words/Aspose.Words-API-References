---
title: "Aspose::Words::DocumentBuilder::InsertField método"
linktitle: "InsertField"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBuilder::InsertField método. Inserta un campo de Word en un documento y opcionalmente actualiza el resultado del campo en C++."
type: docs
weight: 34000
url: /es/cpp/aspose.words/documentbuilder/insertfield/
---
## DocumentBuilder::InsertField(Aspose::Words::Fields::FieldType, bool) method


Inserta un campo de Word en un documento y opcionalmente actualiza el resultado del campo.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(Aspose::Words::Fields::FieldType fieldType, bool updateField)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | El tipo del campo a añadir. |
| updateField | bool | Especifica si se debe actualizar el campo inmediatamente. |

### ReturnValue

Un objeto [Field](../../../aspose.words.fields/field/) que representa el campo insertado.
## Observaciones


Este método inserta un campo en un documento. Aspose.Words puede actualizar campos de la mayoría de los tipos, pero no todos. Para más detalles, vea la sobrecarga [InsertField()](../).

## Ejemplos



Muestra cómo insertar un campo en un documento usando FieldType.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte dos campos pasando una bandera que determina si se actualizan mientras el constructor los inserta.
// En algunos casos, actualizar campos puede ser costoso computacionalmente, y puede ser una buena idea diferir la actualización.
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

    // Necesitaremos actualizar estos campos usando los métodos de actualización manualmente.
    doc->get_Range()->get_Fields()->idx_get(0)->Update();

    ASSERT_EQ(u"John Doe", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

    doc->UpdateFields();

    ASSERT_EQ(u"1", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
}
```

## Ver también

* Class [Field](../../../aspose.words.fields/field/)
* Enum [FieldType](../../../aspose.words.fields/fieldtype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertField(const System::String\&) method


Inserta un campo de Word en un documento y actualiza el resultado del campo.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(const System::String &fieldCode)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fieldCode | const System::String\& | El código de campo a insertar (sin llaves). |

### ReturnValue

Un objeto [Field](../../../aspose.words.fields/field/) que representa el campo insertado.
## Observaciones


Este método inserta un campo en un documento y actualiza el resultado del campo inmediatamente. Aspose.Words puede actualizar campos de la mayoría de los tipos, pero no de todos. Para más detalles, consulte la sobrecarga [InsertField()](../).

## Ejemplos



Muestra cómo insertar campos y mover el cursor del DocumentBuilder a ellos.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertField(u"MERGEFIELD MyMergeField1 \\* MERGEFORMAT");
builder->InsertField(u"MERGEFIELD MyMergeField2 \\* MERGEFORMAT");

// Mueva el cursor al primer MERGEFIELD.
builder->MoveToMergeField(u"MyMergeField1", true, false);

// Tenga en cuenta que el cursor se coloca inmediatamente después del primer MERGEFIELD y antes del segundo.
ASPOSE_ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Start(), builder->get_CurrentNode());
ASPOSE_ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_End(), builder->get_CurrentNode()->get_PreviousSibling());

// Si deseamos editar el código de campo o el contenido del campo usando el builder,
// su cursor tendría que estar dentro de un campo.
// Para colocarlo dentro de un campo, necesitaríamos llamar al método MoveTo del document builder
// y pasar el nodo de inicio o separador del campo como argumento.
builder->Write(u" Text between our merge fields. ");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.MergeFields.docx");
```


Muestra cómo insertar un campo en un documento usando un código de campo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Esta sobrecarga del método InsertField actualiza automáticamente los campos insertados.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```

## Ver también

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertField(const System::String\&, const System::String\&) method


Inserta un campo de Word en un documento sin actualizar el resultado del campo.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(const System::String &fieldCode, const System::String &fieldValue)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fieldCode | const System::String\& | El código de campo a insertar (sin llaves). |
| fieldValue | const System::String\& | El valor del campo a insertar. Pase **null** para los campos que no tienen un valor. |

### ReturnValue

Un objeto [Field](../../../aspose.words.fields/field/) que representa el campo insertado.
## Observaciones


[Fields](../../../aspose.words.fields/) in Microsoft Word documents consist of a field code and a field result. The field code is like a formula and the field result is like the value that the formula produces. The field code may also contain field switches that are like additional instructions to perform a specific action.

Puede alternar entre mostrar códigos de campo y resultados en su documento en Microsoft Word usando el atajo de teclado Alt+F9. Los códigos de campo aparecen entre llaves ( { } ).

Para crear un campo, necesita especificar un tipo de campo, un código de campo y un valor de campo "placeholder". Si no está seguro de la sintaxis de un código de campo en particular, cree el campo primero en Microsoft Word y cambie a ver su código de campo.

Aspose.Words puede calcular resultados de campo para la mayoría de los tipos de campo, pero este método no actualiza el resultado del campo automáticamente. Debido a que el resultado del campo no se calcula automáticamente, se espera que pase algún valor de cadena (o incluso una cadena vacía) que se insertará en el resultado del campo. Este valor permanecerá en el resultado del campo como un marcador de posición hasta que el campo se actualice. Para actualizar el resultado del campo puede llamar a [Update](../../../aspose.words.fields/field/update/) en el objeto de campo devuelto o a [UpdateFields](../../document/updatefields/) para actualizar los campos en todo el documento.

## Ejemplos



Muestra cómo configurar la numeración de páginas en una sección.
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

// Mueva el constructor de documentos al encabezado principal de la primera sección,
// que se mostrará en cada página de esa sección.
builder->MoveToSection(0);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);

// Inserte un campo PAGE, que mostrará el número de la página actual.
builder->Write(u"Page ");
builder->InsertField(u"PAGE", u"");

// Configure la sección para que la cuenta de páginas que muestran los campos PAGE comience en 5.
// Además, configure todos los campos PAGE para que muestren sus números de página usando numerales romanos en mayúsculas.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageStartingNumber(5);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);

// Cree otro encabezado principal para la segunda sección, con otro campo PAGE.
builder->MoveToSection(1);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->Write(u" - ");
builder->InsertField(u"PAGE", u"");
builder->Write(u" - ");

// Configure la sección para que la cuenta de páginas que muestran los campos PAGE comience en 10.
// Además, configure todos los campos PAGE para que muestren sus números de página usando números arábigos.
pageSetup = doc->get_Sections()->idx_get(1)->get_PageSetup();
pageSetup->set_PageStartingNumber(10);
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::Arabic);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageNumbering.docx");
```

## Ver también

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
