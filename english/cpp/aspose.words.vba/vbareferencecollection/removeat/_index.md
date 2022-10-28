---
title: RemoveAt
second_title: Aspose.Words for C++ API Reference
description: Removes the VbaReference element at the specified index of the collection.
type: docs
weight: 92
url: /cpp/aspose.words.vba/vbareferencecollection/removeat/
---
## VbaReferenceCollection.RemoveAt method


Removes the [VbaReference](../../vbareference/) element at the specified index of the collection.

```cpp
void Aspose::Words::Vba::VbaReferenceCollection::RemoveAt(int32_t index)
```


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

