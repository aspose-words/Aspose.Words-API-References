---
title: "Aspose::Words::Revision::get_ParentStyle method"
linktitle: "get_ParentStyle"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Revision::get_ParentStyle method. Возвращает непосредственный родительский стиль (владельца) этой правки. Это свойство будет работать только для типа правки StyleDefinitionChange в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words/revision/get_parentstyle/
---
## Revision::get_ParentStyle method


Возвращает непосредственный родительский стиль (владельца) этой правки. Это свойство будет работать только для типа правки [StyleDefinitionChange](../../revisiontype/).

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::Revision::get_ParentStyle()
```


## Примеры



Показывает, как работать с коллекцией правок документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");
System::SharedPtr<Aspose::Words::RevisionCollection> revisions = doc->get_Revisions();

// Эта коллекция сама содержит коллекцию групп правок.
// Каждая группа представляет собой последовательность смежных правок.
std::cout << System::String::Format(u"{0} revision groups:", revisions->get_Groups()->get_Count()) << std::endl;

// Итерируйте по коллекции групп и выводите текст, к которому относится правка.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::RevisionGroup>>> e = revisions->get_Groups()->GetEnumerator();
    while (e->MoveNext())
    {
        std::cout << (System::String::Format(u"\tGroup type \"{0}\", ", e->get_Current()->get_RevisionType()) + System::String::Format(u"author: {0}, contents: [{1}]", e->get_Current()->get_Author(), e->get_Current()->get_Text().Trim())) << std::endl;
    }
}

// Каждый Run, затронутый правкой, получает соответствующий объект Revision.
// Коллекция правок значительно больше, чем сокращённая форма, которую мы вывели выше,
// в зависимости от того, на сколько Run'ов мы разбили документ во время редактирования в Microsoft Word.
std::cout << System::String::Format(u"\n{0} revisions:", revisions->get_Count()) << std::endl;

{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Revision>>> e = revisions->GetEnumerator();
    while (e->MoveNext())
    {
        // StyleDefinitionChange строго влияет на стили, а не на узлы документа. Это означает, что "ParentStyle"
        // свойство всегда будет использоваться, тогда как ParentNode всегда будет null.
        // Поскольку все остальные изменения влияют на узлы, соответственно ParentNode будет использоваться, а ParentStyle будет null.
        if (e->get_Current()->get_RevisionType() == Aspose::Words::RevisionType::StyleDefinitionChange)
        {
            std::cout << (System::String::Format(u"\tRevision type \"{0}\", ", e->get_Current()->get_RevisionType()) + System::String::Format(u"author: {0}, style: [{1}]", e->get_Current()->get_Author(), e->get_Current()->get_ParentStyle()->get_Name())) << std::endl;
        }
        else
        {
            std::cout << (System::String::Format(u"\tRevision type \"{0}\", ", e->get_Current()->get_RevisionType()) + System::String::Format(u"author: {0}, contents: [{1}]", e->get_Current()->get_Author(), e->get_Current()->get_ParentNode()->GetText().Trim())) << std::endl;
        }
    }
}

// Отклоните все правки через коллекцию, вернув документ к его исходной форме.
revisions->RejectAll();

ASSERT_EQ(0, revisions->get_Count());
```

## См. также

* Class [Style](../../style/)
* Class [Revision](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
