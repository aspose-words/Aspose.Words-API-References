---
title: "Aspose::Words::DocumentBuilder::MoveToMergeField method"
linktitle: "MoveToMergeField"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBuilder::MoveToMergeField method. Mueve el cursor a una posición justo más allá del campo de combinación especificado y elimina el campo de combinación en C++."
type: docs
weight: 58000
url: /es/cpp/aspose.words/documentbuilder/movetomergefield/
---
## DocumentBuilder::MoveToMergeField(const System::String\&) method


Mueve el cursor a una posición justo después del campo de combinación especificado y elimina el campo de combinación.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToMergeField(const System::String &fieldName)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fieldName | const System::String\& | El nombre del campo de combinación de correspondencia, sin distinción de mayúsculas y minúsculas. |

### ReturnValue

**true** if the merge field was found and the cursor was moved; **false** otherwise.
## Observaciones


Nota que este método elimina el campo de combinación del documento después de mover el cursor.

## Ejemplos



Muestra cómo rellenar MERGEFIELDs con datos usando un constructor de documentos en lugar de una combinación de correspondencia.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte algunos MERGEFIELDS, que aceptan datos de columnas con el mismo nombre en una fuente de datos durante una combinación de correspondencia,
// y luego rellénelos manualmente.
builder->InsertField(u" MERGEFIELD Chairman ");
builder->InsertField(u" MERGEFIELD ChiefFinancialOfficer ");
builder->InsertField(u" MERGEFIELD ChiefTechnologyOfficer ");

builder->MoveToMergeField(u"Chairman");
builder->set_Bold(true);
builder->Writeln(u"John Doe");

builder->MoveToMergeField(u"ChiefFinancialOfficer");
builder->set_Italic(true);
builder->Writeln(u"Jane Doe");

builder->MoveToMergeField(u"ChiefTechnologyOfficer");
builder->set_Italic(true);
builder->Writeln(u"John Bloggs");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.FillMergeFields.docx");
```

## Ver también

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::MoveToMergeField(const System::String\&, bool, bool) method


Mueve el campo de combinación al campo de combinación especificado.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToMergeField(const System::String &fieldName, bool isAfter, bool isDeleteField)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fieldName | const System::String\& | El nombre del campo de combinación de correspondencia, sin distinción de mayúsculas y minúsculas. |
| isAfter | bool | Cuando **true**, mueve el cursor para que quede después del final del campo. Cuando **false**, mueve el cursor para que quede antes del inicio del campo. |
| isDeleteField | bool | Cuando **true**, elimina el campo de combinación. |

### ReturnValue

**true** if the merge field was found and the cursor was moved; **false** otherwise.

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

## Ver también

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
