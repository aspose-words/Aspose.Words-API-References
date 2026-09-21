---
title: "Aspose::Words::DocumentBuilder::MoveToField metod"
linktitle: "MoveToField"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::MoveToField metod. Flyttar markören till ett fält i dokumentet i C++."
type: docs
weight: 56000
url: /sv/cpp/aspose.words/documentbuilder/movetofield/
---
## DocumentBuilder::MoveToField method


Flyttar markören till ett fält i dokumentet.

```cpp
void Aspose::Words::DocumentBuilder::MoveToField(const System::SharedPtr<Aspose::Words::Fields::Field> &field, bool isAfter)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fält | const System::SharedPtr\<Aspose::Words::Fields::Field\>\& | Fältet att flytta markören till. |
| isAfter | bool | När **true**, flyttar markören till efter fältets slut. När **false**, flyttar markören till före fältets början. |

## Exempel



Visar hur man flyttar en dokumentbyggares nodinfogningspunktmarkör till ett specifikt fält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga ett fält med DocumentBuilder och lägg till en textsekvens efter det.
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" AUTHOR \"John Doe\" ");

// Byggarens markör är för närvarande i slutet av dokumentet.
ASSERT_TRUE(System::TestTools::IsNull(builder->get_CurrentNode()));

// Flytta markören till fältet samtidigt som du anger om markören ska placeras före eller efter fältet.
builder->MoveToField(field, moveCursorToAfterTheField);

// Observera att markören är utanför fältet i båda fallen.
// Detta betyder att vi inte kan redigera fältet med byggaren på detta sätt.
// För att redigera ett fält kan vi använda byggarens MoveTo‑metod på ett fälts **FieldStart**
// eller **FieldSeparator**‑nod för att placera markören inuti.
if (moveCursorToAfterTheField)
{
    ASSERT_TRUE(System::TestTools::IsNull(builder->get_CurrentNode()));
    builder->Write(u" Text immediately after the field.");

    ASSERT_EQ(u"\u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015 Text immediately after the field.", doc->GetText().Trim());
}
else
{
    ASPOSE_ASSERT_EQ(field->get_Start(), builder->get_CurrentNode());
    builder->Write(u"Text immediately before the field. ");

    ASSERT_EQ(u"Text immediately before the field. \u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015", doc->GetText().Trim());
}
```

## Se även

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
