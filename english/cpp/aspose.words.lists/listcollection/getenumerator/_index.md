---
title: GetEnumerator
second_title: Aspose.Words for C++ API Reference
description: Gets the enumerator object that will enumerate lists in the document.
type: docs
weight: 118
url: /cpp/aspose.words.lists/listcollection/getenumerator/
---
## ListCollection::GetEnumerator method


Gets the enumerator object that will enumerate lists in the document.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Lists::List>>> Aspose::Words::Lists::ListCollection::GetEnumerator() override
```


## Examples



Shows how to create a document with a sample of all the lists from another document. 
```cpp
void PrintOutAllLists()
{
    auto srcDoc = MakeObject<Document>(MyDir + u"Rendering.docx");

    auto dstDoc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(dstDoc);

    for (const auto& srcList : srcDoc->get_Lists())
    {
        SharedPtr<List> dstList = dstDoc->get_Lists()->AddCopy(srcList);
        AddListSample(builder, dstList);
    }

    dstDoc->Save(ArtifactsDir + u"Lists.PrintOutAllLists.docx");
}

static void AddListSample(SharedPtr<DocumentBuilder> builder, SharedPtr<List> list)
{
    builder->Writeln(String(u"Sample formatting of list with ListId:") + list->get_ListId());
    builder->get_ListFormat()->set_List(list);
    for (int i = 0; i < list->get_ListLevels()->get_Count(); i++)
    {
        builder->get_ListFormat()->set_ListLevelNumber(i);
        builder->Writeln(String(u"Level ") + i);
    }

    builder->get_ListFormat()->RemoveNumbers();
    builder->Writeln();
}
```

## See Also

* Class [List](../../list/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words](../../../)
