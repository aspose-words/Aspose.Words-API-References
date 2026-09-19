---
title: "Aspose::Words::BorderCollection::GetEnumerator metodo"
linktitle: "GetEnumerator"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::BorderCollection::GetEnumerator. Restituisce un oggetto enumeratore che può essere usato per iterare su tutti i bordi nella collezione in C++."
type: docs
weight: 16000
url: /it/cpp/aspose.words/bordercollection/getenumerator/
---
## BorderCollection::GetEnumerator method


Restituisce un oggetto enumeratore che può essere usato per iterare su tutti i bordi nella raccolta.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Border>>> Aspose::Words::BorderCollection::GetEnumerator() override
```


## Esempi



Mostra come iterare e modificare tutti i bordi in un oggetto di formato paragrafo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Configura le impostazioni di formato paragrafo del builder per creare un bordo a onda verde su tutti i lati.
System::SharedPtr<Aspose::Words::BorderCollection> borders = builder->get_ParagraphFormat()->get_Borders();

{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Border>>> enumerator = borders->GetEnumerator();
    while (enumerator->MoveNext())
    {
        System::SharedPtr<Aspose::Words::Border> border = enumerator->get_Current();
        border->set_Color(System::Drawing::Color::get_Green());
        border->set_LineStyle(Aspose::Words::LineStyle::Wave);
        border->set_LineWidth(3);
    }
}

// Inserisci un paragrafo. Le nostre impostazioni del bordo determineranno l'aspetto del suo bordo.
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"BorderCollection.GetBordersEnumerator.docx");
```

## Vedi anche

* Class [Border](../../border/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
