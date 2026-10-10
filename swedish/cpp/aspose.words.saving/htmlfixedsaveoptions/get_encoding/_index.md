---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding‑metod"
linktitle: "get_Encoding"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding‑metod. Anger kodningen som ska användas vid export till HTML. Standardvärdet är new UTF8Encoding(true) (UTF‑8 med BOM) i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.saving/htmlfixedsaveoptions/get_encoding/
---
## HtmlFixedSaveOptions::get_Encoding method


Anger kodningen som ska användas vid export till HTML. Standardvärdet är **new UTF8Encoding(true)** (UTF-8 med BOM).

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding() const
```


## Exempel



Visar hur man anger vilken kodning som ska användas vid export av ett dokument till HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello World!");

// Standardkodningen är UTF-8. Om vi vill representera vårt dokument med en annan kodning,
// kan vi använda ett SaveOptions‑objekt för att ange en specifik kodning.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_Encoding(System::Text::Encoding::get_ASCII());

ASSERT_EQ(u"US-ASCII", htmlFixedSaveOptions->get_Encoding()->get_EncodingName());

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

## Se även

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
