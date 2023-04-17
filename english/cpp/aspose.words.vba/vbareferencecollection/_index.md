---
title: Aspose::Words::Vba::VbaReferenceCollection class
linktitle: VbaReferenceCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Vba::VbaReferenceCollection class. Represents a collection of VbaReference objects. To learn more, visit the  documentation article in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.vba/vbareferencecollection/
---
## VbaReferenceCollection class


Represents a collection of [VbaReference](../vbareference/) objects. To learn more, visit the [Working with VBA Macros](https://docs.aspose.com/words/cpp/working-with-vba-macros/) documentation article.

```cpp
class VbaReferenceCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Vba::VbaReference>>
```

## Methods

| Method | Description |
| --- | --- |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Returns the number of VBA references in the collection. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Gets [VbaReference](../vbareference/) object at the specified index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Vba::VbaReference\>\&) | Removes the first occurrence of a specified [VbaReference](../vbareference/) item from the collection. |
| [RemoveAt](./removeat/)(int32_t) | Removes the [VbaReference](../vbareference/) element at the specified index of the collection. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Description |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |

## Examples



Shows how to get/remove an element from the VBA reference collection. 
```cpp
void RemoveVbaReference()
{
    const String brokenPath = u"X:\\broken.dll";
    auto doc = MakeObject<Document>(MyDir + u"VBA project.docm");

    SharedPtr<VbaReferenceCollection> references = doc->get_VbaProject()->get_References();
    ASSERT_EQ(5, references->get_Count());

    for (int i = references->get_Count() - 1; i >= 0; i--)
    {
        SharedPtr<VbaReference> reference = doc->get_VbaProject()->get_References()->idx_get(i);
        String path = GetLibIdPath(reference);

        if (path == brokenPath)
        {
            references->RemoveAt(i);
        }
    }
    ASSERT_EQ(4, references->get_Count());

    references->Remove(references->idx_get(1));
    ASSERT_EQ(3, references->get_Count());

    doc->Save(ArtifactsDir + u"VbaProject.RemoveVbaReference.docm");
}

static String GetLibIdPath(SharedPtr<VbaReference> reference)
{
    switch (reference->get_Type())
    {
    case VbaReferenceType::Registered:
    case VbaReferenceType::Original:
    case VbaReferenceType::Control:
        return GetLibIdReferencePath(reference->get_LibId());

    case VbaReferenceType::Project:
        return GetLibIdProjectPath(reference->get_LibId());

    default:
        throw System::ArgumentOutOfRangeException();
    }
}

static String GetLibIdReferencePath(String libIdReference)
{
    if (libIdReference != nullptr)
    {
        ArrayPtr<String> refParts = libIdReference.Split(MakeArray<char16_t>({u'#'}));
        if (refParts->get_Length() > 3)
        {
            return refParts[3];
        }
    }

    return u"";
}

static String GetLibIdProjectPath(String libIdProject)
{
    return libIdProject != nullptr ? libIdProject.Substring(3) : u"";
}
```

## See Also

* Namespace [Aspose::Words::Vba](../)
* Library [Aspose.Words for C++](../../)
