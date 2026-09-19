---
title: "Metodo Aspose::Words::Drawing::ShapeBase::get_IsImage"
linktitle: "get_IsImage"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::ShapeBase::get_IsImage. Restituisce true se questa forma è una forma immagine in C++."
type: docs
weight: 29000
url: /it/cpp/aspose.words.drawing/shapebase/get_isimage/
---
## ShapeBase::get_IsImage method


Restituisce **true** se questa forma è una forma immagine.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsImage()
```


## Esempi



Mostra come aprire un documento HTML con immagini da uno stream utilizzando un URI di base.
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.html");
    // Passa l'URI della cartella di base durante il caricamento.
    // in modo che tutte le immagini con URI relativi nel documento HTML possano essere trovate.
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    loadOptions->set_BaseUri(get_ImageDir());

    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Verifica che la prima forma del documento contenga un'immagine valida.
    auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

    ASSERT_TRUE(shape->get_IsImage());
    ASSERT_FALSE(System::TestTools::IsNull(shape->get_ImageData()->get_ImageBytes()));
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Width()), 0.01);
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Height()), 0.01);
}
```

## Vedi anche

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
