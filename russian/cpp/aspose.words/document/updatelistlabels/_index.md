---
title: "Метод Aspose::Words::Document::UpdateListLabels"
linktitle: "UpdateListLabels"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Document::UpdateListLabels. Обновляет метки списков для всех элементов списка в документе на C++."
type: docs
weight: 97000
url: /ru/cpp/aspose.words/document/updatelistlabels/
---
## Document::UpdateListLabels method


Обновляет метки списков для всех элементов списка в документе.

```cpp
void Aspose::Words::Document::UpdateListLabels()
```

## Примечания


Этот метод обновляет свойства меток списка, такие как [LabelValue](../../../aspose.words.lists/listlabel/get_labelvalue/) и [LabelString](../../../aspose.words.lists/listlabel/get_labelstring/) для каждого объекта [ListLabel](../../paragraph/get_listlabel/) в документе.

Также этот метод иногда вызывается неявно при обновлении полей в документе. Это необходимо, потому что некоторые поля, которые могут ссылаться на номера списков (например, TOC или REF), должны быть актуальными.

## Примеры



Показывает, как извлечь метки списка из всех абзацев, являющихся элементами списка.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
doc->UpdateListLabels();

System::SharedPtr<Aspose::Words::NodeCollection> paras = doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true);

// Найдите, есть ли у нас список в абзаце. В нашем документе список использует обычные арабские цифры,
// которые начинаются с трёх и заканчиваются на шести.
for (auto&& paragraph : paras->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()->LINQ_Where(static_cast<System::Func<System::SharedPtr<Aspose::Words::Paragraph>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Paragraph> p)>>([](System::SharedPtr<Aspose::Words::Paragraph> p) -> bool
{
    return p->get_ListFormat()->get_IsListItem();
})))->LINQ_ToList())
{
    std::cout << System::String::Format(u"List item paragraph #{0}", paras->IndexOf(paragraph)) << std::endl;

    // Это текст, который мы получаем при выводе этого узла в текстовый формат.
    // Этот вывод текста будет опускать метки списка. Удалите любые символы форматирования абзаца.
    System::String paragraphText = paragraph->ToString(Aspose::Words::SaveFormat::Text).Trim();
    std::cout << System::String::Format(u"\tExported Text: {0}", paragraphText) << std::endl;

    System::SharedPtr<Aspose::Words::Lists::ListLabel> label = paragraph->get_ListLabel();

    // Это получает позицию абзаца на текущем уровне списка. Если у нас есть список с несколькими уровнями,
    // это покажет, какую позицию он занимает на этом уровне.
    std::cout << System::String::Format(u"\tNumerical Id: {0}", label->get_LabelValue()) << std::endl;

    // Объедините их, чтобы включить метку списка вместе с текстом в выводе.
    std::cout << System::String::Format(u"\tList label combined with text: {0} {1}", label->get_LabelString(), paragraphText) << std::endl;
}
```

## См. также

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
