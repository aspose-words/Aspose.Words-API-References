---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding metodo"
linktitle: "get_Encoding"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding metodo. Specifica la codifica da utilizzare durante l'esportazione in HTML. Il valore predefinito è new UTF8Encoding(true) (UTF-8 con BOM) in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.saving/htmlfixedsaveoptions/get_encoding/
---
## HtmlFixedSaveOptions::get_Encoding method


Specifica la codifica da utilizzare durante l'esportazione in HTML. Il valore predefinito è **new UTF8Encoding(true)** (UTF-8 con BOM).

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding() const
```


## Esempi



Mostra come impostare quale codifica utilizzare durante l'esportazione di un documento in HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello World!");

// La codifica predefinita è UTF-8. Se desideriamo rappresentare il nostro documento usando una codifica diversa,
// possiamo utilizzare un oggetto SaveOptions per impostare una codifica specifica.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_Encoding(System::Text::Encoding::get_ASCII());

ASSERT_EQ(u"US-ASCII", htmlFixedSaveOptions->get_Encoding()->get_EncodingName());

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

## Vedi anche

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
