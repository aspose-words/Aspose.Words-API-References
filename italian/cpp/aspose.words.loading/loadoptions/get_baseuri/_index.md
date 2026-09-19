---
title: "Aspose::Words::Loading::LoadOptions::get_BaseUri metodo"
linktitle: "get_BaseUri"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Loading::LoadOptions::get_BaseUri metodo. Ottiene o imposta la stringa che verrà utilizzata per risolvere gli URI relativi trovati nel documento in URI assoluti quando necessario. Può essere null o una stringa vuota. Il valore predefinito è null in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.loading/loadoptions/get_baseuri/
---
## LoadOptions::get_BaseUri method


Ottiene o imposta la stringa che verrà utilizzata per risolvere gli URI relativi trovati nel documento in URI assoluti quando necessario. Può essere **null** o una stringa vuota. Il valore predefinito è **null**.

```cpp
System::String Aspose::Words::Loading::LoadOptions::get_BaseUri() const
```

## Note


Questa proprietà è utilizzata per risolvere gli URI relativi in assoluti nei seguenti casi:

1. Quando si carica un documento HTML da uno stream e il documento contiene immagini con URI relativi e non ha un URI di base specificato nell'elemento BASE dell'HTML.
1. Quando si salva un documento in PDF e altri formati, per recuperare le immagini collegate tramite URI relativi in modo che le immagini possano essere salvate nel documento di output.



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

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
