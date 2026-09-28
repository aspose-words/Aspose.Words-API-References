---
title: "Aspose::Words::Loading::LoadOptions::get_BaseUri метод"
linktitle: "get_BaseUri"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Loading::LoadOptions::get_BaseUri метод. Получает или задаёт строку, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI при необходимости. Может быть null или пустой строкой. По умолчанию — null в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.loading/loadoptions/get_baseuri/
---
## LoadOptions::get_BaseUri method


Получает или задает строку, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI при необходимости. Может быть **null** или пустой строкой. По умолчанию **null**.

```cpp
System::String Aspose::Words::Loading::LoadOptions::get_BaseUri() const
```

## Примечания


Это свойство используется для преобразования относительных URI в абсолютные в следующих случаях:

1. При загрузке HTML‑документа из потока, если документ содержит изображения с относительными URI и не имеет базового URI, указанного в элементе BASE HTML.
1. При сохранении документа в PDF и другие форматы, чтобы получить изображения, связанные с помощью относительных URI, чтобы их можно было сохранить в выходном документе.



## Примеры



Показывает, как открыть HTML‑документ с изображениями из потока, используя базовый URI.
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.html");
    // Передайте URI базовой папки при загрузке.
    // чтобы любые изображения с относительными URI в HTML‑документе могли быть найдены.
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    loadOptions->set_BaseUri(get_ImageDir());

    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Убедитесь, что первая фигура документа содержит действительное изображение.
    auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

    ASSERT_TRUE(shape->get_IsImage());
    ASSERT_FALSE(System::TestTools::IsNull(shape->get_ImageData()->get_ImageBytes()));
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Width()), 0.01);
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Height()), 0.01);
}
```

## См. также

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
