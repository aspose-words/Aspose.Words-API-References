---
title: "Aspose::Words::Drawing::ShapeBase::get_IsImage Methode"
linktitle: "get_IsImage"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_IsImage Methode. Gibt true zurück, wenn diese Form eine Bildform ist in C++."
type: docs
weight: 29000
url: /de/cpp/aspose.words.drawing/shapebase/get_isimage/
---
## ShapeBase::get_IsImage method


Gibt **true** zurück, wenn diese Form eine Bildform ist.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsImage()
```


## Beispiele



Zeigt, wie man ein HTML-Dokument mit Bildern aus einem Stream unter Verwendung einer Basis-URI öffnet.
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.html");
    // Übergeben Sie beim Laden die URI des Basisordners
    // damit alle Bilder mit relativen URIs im HTML-Dokument gefunden werden können.
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    loadOptions->set_BaseUri(get_ImageDir());

    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Überprüfen Sie, dass die erste Form des Dokuments ein gültiges Bild enthält.
    auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

    ASSERT_TRUE(shape->get_IsImage());
    ASSERT_FALSE(System::TestTools::IsNull(shape->get_ImageData()->get_ImageBytes()));
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Width()), 0.01);
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Height()), 0.01);
}
```

## Siehe auch

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
