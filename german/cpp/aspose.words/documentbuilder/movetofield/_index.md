---
title: "Aspose::Words::DocumentBuilder::MoveToField Methode"
linktitle: "MoveToField"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::MoveToField Methode. Bewegt den Cursor zu einem Feld im Dokument in C++."
type: docs
weight: 56000
url: /de/cpp/aspose.words/documentbuilder/movetofield/
---
## DocumentBuilder::MoveToField method


Bewegt den Cursor zu einem Feld im Dokument.

```cpp
void Aspose::Words::DocumentBuilder::MoveToField(const System::SharedPtr<Aspose::Words::Fields::Field> &field, bool isAfter)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| field | const System::SharedPtr\<Aspose::Words::Fields::Field\>\& | Das Feld, zu dem der Cursor bewegt werden soll. |
| isAfter | bool | Wenn **true**, wird der Cursor nach dem Feldende positioniert. Wenn **false**, wird der Cursor vor dem Feldanfang positioniert. |

## Beispiele



Zeigt, wie der Knoten‑Einfügepunkt‑Cursor eines DocumentBuilder zu einem bestimmten Feld bewegt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie ein Feld mit dem DocumentBuilder ein und fügen Sie danach einen Textlauf hinzu.
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" AUTHOR \"John Doe\" ");

// Der Cursor des Builders befindet sich derzeit am Ende des Dokuments.
ASSERT_TRUE(System::TestTools::IsNull(builder->get_CurrentNode()));

// Bewegen Sie den Cursor zum Feld und geben Sie dabei an, ob der Cursor vor oder nach dem Feld platziert werden soll.
builder->MoveToField(field, moveCursorToAfterTheField);

// Beachten Sie, dass der Cursor in beiden Fällen außerhalb des Feldes liegt.
// Das bedeutet, dass wir das Feld nicht auf diese Weise mit dem Builder bearbeiten können.
// Um ein Feld zu bearbeiten, können wir die MoveTo-Methode des Builders auf dem FieldStart eines Feldes verwenden
// oder den FieldSeparator-Knoten, um den Cursor darin zu platzieren.
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

## Siehe auch

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
