---
title: "Aspose::Words::Drawing::OleFormat::get_SuggestedFileName метод"
linktitle: "get_SuggestedFileName"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::OleFormat::get_SuggestedFileName метод. Получает предложенное имя файла для текущего встроенного объекта, если вы хотите сохранить его в файл в C++."
type: docs
weight: 14000
url: /ru/cpp/aspose.words.drawing/oleformat/get_suggestedfilename/
---
## OleFormat::get_SuggestedFileName method


Получает рекомендуемое имя файла для текущего встроенного объекта, если вы хотите сохранить его в файл.

```cpp
System::String Aspose::Words::Drawing::OleFormat::get_SuggestedFileName()
```


## Примеры



Показывает, как получить предложенное имя файла объекта OLE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE shape.rtf");

auto oleShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->get_FirstSection()->get_Body()->GetChild(Aspose::Words::NodeType::Shape, 0, true));

// Объекты OLE могут предоставлять предложенное имя файла и расширение,
// которые мы можем использовать при сохранении содержимого объекта в файл в локальной файловой системе.
System::String suggestedFileName = oleShape->get_OleFormat()->get_SuggestedFileName();

ASSERT_EQ(u"CSV.csv", suggestedFileName);

{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + suggestedFileName, System::IO::FileMode::Create);
    oleShape->get_OleFormat()->Save(fileStream);
}
```

## См. также

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
