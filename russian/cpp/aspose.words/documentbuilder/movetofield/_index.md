---
title: "Aspose::Words::DocumentBuilder::MoveToField метод"
linktitle: "MoveToField"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBuilder::MoveToField метод. Перемещает курсор к полю в документе в C++."
type: docs
weight: 56000
url: /ru/cpp/aspose.words/documentbuilder/movetofield/
---
## DocumentBuilder::MoveToField method


Перемещает курсор к полю в документе.

```cpp
void Aspose::Words::DocumentBuilder::MoveToField(const System::SharedPtr<Aspose::Words::Fields::Field> &field, bool isAfter)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| поле | const System::SharedPtr\<Aspose::Words::Fields::Field\>\& | Поле, к которому нужно переместить курсор. |
| isAfter | bool | Когда **true**, перемещает курсор после конца поля. Когда **false**, перемещает курсор перед началом поля. |

## Примеры



Показывает, как переместить курсор точки вставки узла document builder к конкретному полю.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте поле с помощью DocumentBuilder и добавьте после него последовательность текста.
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" AUTHOR \"John Doe\" ");

// Курсор builder'а в данный момент находится в конце документа.
ASSERT_TRUE(System::TestTools::IsNull(builder->get_CurrentNode()));

// Переместите курсор к полю, указав, разместить ли курсор перед полем или после него.
builder->MoveToField(field, moveCursorToAfterTheField);

// Обратите внимание, что курсор находится за пределами поля в обоих случаях.
// Это означает, что мы не можем редактировать поле с помощью builder'а таким образом.
// Чтобы отредактировать поле, мы можем использовать метод MoveTo builder'а на FieldStart поля
// или узел FieldSeparator, чтобы разместить курсор внутри.
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

## См. также

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
