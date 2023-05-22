---
title: Aspose::Words::Drawing::OleFormat::get_SuggestedFileName method
linktitle: get_SuggestedFileName
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::OleFormat::get_SuggestedFileName method. Gets the file name suggested for the current embedded object if you want to save it into a file in C++.'
type: docs
weight: 14000
url: /cpp/aspose.words.drawing/oleformat/get_suggestedfilename/
---
## OleFormat::get_SuggestedFileName method


Gets the file name suggested for the current embedded object if you want to save it into a file.

```cpp
System::String Aspose::Words::Drawing::OleFormat::get_SuggestedFileName()
```


## Examples



Shows how to get an OLE object's suggested file name. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"OLE shape.rtf");

auto oleShape = System::ExplicitCast<Shape>(doc->get_FirstSection()->get_Body()->GetChild(NodeType::Shape, 0, true));

// OLE objects can provide a suggested filename and extension,
// which we can use when saving the object's contents into a file in the local file system.
String suggestedFileName = oleShape->get_OleFormat()->get_SuggestedFileName();

ASSERT_EQ(u"CSV.csv", suggestedFileName);

{
    auto fileStream = MakeObject<System::IO::FileStream>(ArtifactsDir + suggestedFileName, System::IO::FileMode::Create);
    oleShape->get_OleFormat()->Save(fileStream);
}
```

## See Also

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
