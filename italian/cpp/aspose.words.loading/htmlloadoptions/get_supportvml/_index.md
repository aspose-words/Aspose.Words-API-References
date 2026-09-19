---
title: "Metodo Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml"
linktitle: "get_SupportVml"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml. Ottiene o imposta un valore che indica se supportare le immagini VML in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.loading/htmlloadoptions/get_supportvml/
---
## HtmlLoadOptions::get_SupportVml method


Ottiene o imposta un valore che indica se supportare le immagini VML.

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml() const
```


## Esempi



Mostra come supportare i commenti condizionali durante il caricamento di un documento HTML.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();

// Se il valore è true, allora consideriamo il codice VML durante l'analisi del documento caricato.
loadOptions->set_SupportVml(supportVml);

// Questo documento contiene un'immagine JPEG all'interno dei tag "<!--[if gte vml 1]>",
// e un'immagine PNG diversa all'interno dei tag "<![if !vml]>".
// Se impostiamo il flag "SupportVml" su "true", Aspose.Words caricherà il JPEG.
// Se impostiamo questo flag su "false", Aspose.Words caricherà solo il PNG.
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

## Vedi anche

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
