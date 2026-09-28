---
title: "Метод Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields"
linktitle: "get_IgnoreFields"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields. Получает или задает логическое значение, указывающее, следует ли игнорировать текст внутри полей. Значение по умолчанию — false в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words.replacing/findreplaceoptions/get_ignorefields/
---
## FindReplaceOptions::get_IgnoreFields method


Получает или задает логическое значение, указывающее, следует ли игнорировать текст внутри полей. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields() const
```

## Примечания


Эта опция влияет на всё поле (все узлы между [FieldStart](../../../aspose.words/nodetype/) и [FieldEnd](../../../aspose.words/nodetype/)).

Чтобы игнорировать только коды полей, пожалуйста, используйте соответствующую опцию [IgnoreFieldCodes](../get_ignorefieldcodes/).

## Примеры



Показывает, как игнорировать текст внутри полей.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->InsertField(u"QUOTE", u"Hello again!");

// Мы можем использовать объект "FindReplaceOptions" для изменения процесса поиска и замены.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Установите флаг "IgnoreFields" в "true", чтобы выполнить поиск и замену
// операцию, игнорирующую текст внутри полей.
// Установите флаг "IgnoreFields" в "false", чтобы выполнить поиск и замену
// операцию, также ищущую текст внутри полей.
options->set_IgnoreFields(ignoreTextInsideFields);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideFields ? System::String(u"Greetings world!\r\u0013QUOTE\u0014Hello again!\u0015") : System::String(u"Greetings world!\r\u0013QUOTE\u0014Greetings again!\u0015"), doc->GetText().Trim());
```

## См. также

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
