---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml Methode"
linktitle: "get_SupportVml"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml method. Ruft einen Wert ab oder legt ihn fest, der angibt, ob VML-Bilder in C++ unterstützt werden."
type: docs
weight: 7000
url: /de/cpp/aspose.words.loading/htmlloadoptions/get_supportvml/
---
## HtmlLoadOptions::get_SupportVml method


Liest oder setzt einen Wert, der angibt, ob VML‑Bilder unterstützt werden.

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml() const
```


## Beispiele



Zeigt, wie bedingte Kommentare beim Laden eines HTML-Dokuments unterstützt werden.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();

// Wenn der Wert true ist, berücksichtigen wir VML-Code beim Parsen des geladenen Dokuments.
loadOptions->set_SupportVml(supportVml);

// Dieses Dokument enthält ein JPEG-Bild innerhalb von "<!--[if gte vml 1]>"-Tags,
// und ein anderes PNG-Bild innerhalb von "<![if !vml]>"-Tags.
// Wenn wir das Flag "SupportVml" auf "true" setzen, lädt Aspose.Words das JPEG.
// Wenn wir dieses Flag auf "false" setzen, lädt Aspose.Words nur das PNG.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VML conditional.htm", loadOptions);

if (supportVml)
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
else
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
```

## Siehe auch

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
