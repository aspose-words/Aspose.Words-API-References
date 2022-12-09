---
title: VbaReference
second_title: Aspose.Words for C++ API Reference
description: Implements a reference to an Automation type library or VBA project. To learn more, visit the  documentation article.
type: docs
weight: 40
url: /cpp/aspose.words.vba/vbareference/
---
## VbaReference class


Implements a reference to an Automation type library or VBA project. To learn more, visit the [Working with VBA Macros](https://docs.aspose.com/words/cpp/working-with-vba-macros/) documentation article.

```cpp
class VbaReference : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| virtual [get_LibId](./get_libid/)() const | Gets a string value containing the identifier of an Automation type library. |
| virtual [get_Type](./get_type/)() | Gets [VbaReferenceType](../vbareferencetype/) object that indicates the type of reference that a [VbaReference](./) object represents. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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
* Library [Aspose.Words](../../)
