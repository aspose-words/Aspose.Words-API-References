---
title: "Aspose::Words::Loading::LoadOptions::get_BaseUri Methode"
linktitle: "get_BaseUri"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::LoadOptions::get_BaseUri Methode. Gibt die Zeichenfolge zurück oder legt sie fest, die verwendet wird, um relative URIs im Dokument bei Bedarf in absolute URIs aufzulösen. Kann null oder eine leere Zeichenfolge sein. Der Standardwert ist null in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.loading/loadoptions/get_baseuri/
---
## LoadOptions::get_BaseUri method


Liest oder setzt die Zeichenfolge, die verwendet wird, um relative URIs im Dokument bei Bedarf in absolute URIs aufzulösen. Kann **null** oder eine leere Zeichenfolge sein. Standard ist **null**.

```cpp
System::String Aspose::Words::Loading::LoadOptions::get_BaseUri() const
```

## Hinweise


Diese Eigenschaft wird verwendet, um relative URIs in den folgenden Fällen in absolute umzuwandeln:

1. Beim Laden eines HTML-Dokuments aus einem Stream, wenn das Dokument Bilder mit relativen URIs enthält und keine Basis-URI im BASE‑HTML‑Element angegeben ist.
1. Beim Speichern eines Dokuments als PDF und in anderen Formaten, um über relative URIs verknüpfte Bilder abzurufen, damit die Bilder im Ausgabedokument gespeichert werden können.



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

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
