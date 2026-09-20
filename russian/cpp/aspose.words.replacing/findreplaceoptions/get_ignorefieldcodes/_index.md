---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes метод"
linktitle: "get_IgnoreFieldCodes"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes метод. Получает или задает логическое значение, указывающее, следует ли игнорировать текст внутри кодов полей. Значение по умолчанию — false в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words.replacing/findreplaceoptions/get_ignorefieldcodes/
---
## FindReplaceOptions::get_IgnoreFieldCodes method


Получает или задает логическое значение, указывающее, следует ли игнорировать текст внутри кодов полей. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes() const
```

## Примечания


Эта опция влияет только на коды полей (она не игнорирует узлы между [FieldSeparator](../../../aspose.words/nodetype/) и [FieldEnd](../../../aspose.words/nodetype/)).

Чтобы игнорировать всё поле, пожалуйста, используйте соответствующую опцию [IgnoreFields](../get_ignorefields/).

## Примеры



Показывает, как игнорировать текст внутри кодов полей.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertField(u"INCLUDETEXT", u"Test IT!");

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreFieldCodes(ignoreFieldCodes);

// Заменить 'T' в документе, игнорируя текст внутри кода поля, или нет.
doc->get_Range()->Replace(System::MakeObject<System::Text::RegularExpressions::Regex>(u"T"), u"*", options);
std::cout << doc->GetText() << std::endl;

ASSERT_EQ(ignoreFieldCodes ? System::String(u"\u0013INCLUDETEXT\u0014*est I*!\u0015") : System::String(u"\u0013INCLUDE*EX*\u0014*est I*!\u0015"), doc->GetText().Trim());
```

## См. также

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
