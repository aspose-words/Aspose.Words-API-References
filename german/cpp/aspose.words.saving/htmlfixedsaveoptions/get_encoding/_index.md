---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding Methode"
linktitle: "get_Encoding"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding Methode. Gibt die zu verwendende Kodierung beim Export nach HTML an. Der Standardwert ist new UTF8Encoding(true) (UTF‑8 mit BOM) in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.saving/htmlfixedsaveoptions/get_encoding/
---
## HtmlFixedSaveOptions::get_Encoding method


Gibt die zu verwendende Kodierung beim Exportieren nach HTML an. Standardwert ist **new UTF8Encoding(true)** (UTF-8 mit BOM).

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding() const
```


## Beispiele



Zeigt, wie die zu verwendende Kodierung beim Export eines Dokuments nach HTML festgelegt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello World!");

// Die Standardkodierung ist UTF‑8. Wenn wir unser Dokument mit einer anderen Kodierung darstellen möchten,
// können wir ein SaveOptions‑Objekt verwenden, um eine bestimmte Kodierung festzulegen.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_Encoding(System::Text::Encoding::get_ASCII());

ASSERT_EQ(u"US-ASCII", htmlFixedSaveOptions->get_Encoding()->get_EncodingName());

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

## Siehe auch

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
