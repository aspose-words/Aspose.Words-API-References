---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding méthode"
linktitle: "get_Encoding"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding méthode. Spécifie l'encodage à utiliser lors de l'exportation vers HTML. La valeur par défaut est new UTF8Encoding(true) (UTF-8 avec BOM) en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.saving/htmlfixedsaveoptions/get_encoding/
---
## HtmlFixedSaveOptions::get_Encoding method


Spécifie l'encodage à utiliser lors de l'exportation vers HTML. La valeur par défaut est **new UTF8Encoding(true)** (UTF-8 avec BOM).

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding() const
```


## Exemples



Montre comment définir l'encodage à utiliser lors de l'exportation d'un document vers HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello World!");

// L'encodage par défaut est UTF-8. Si nous voulons représenter notre document en utilisant un encodage différent,
// nous pouvons utiliser un objet SaveOptions pour définir un encodage spécifique.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_Encoding(System::Text::Encoding::get_ASCII());

ASSERT_EQ(u"US-ASCII", htmlFixedSaveOptions->get_Encoding()->get_EncodingName());

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

## Voir aussi

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
