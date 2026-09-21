---
title: "Aspose::Words::BorderCollection::GetEnumerator metod"
linktitle: "GetEnumerator"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::BorderCollection::GetEnumerator metod. Returnerar ett enumerator-objekt som kan användas för att iterera över alla kanter i samlingen i C++."
type: docs
weight: 16000
url: /sv/cpp/aspose.words/bordercollection/getenumerator/
---
## BorderCollection::GetEnumerator method


Returnerar ett enumeratorobjekt som kan användas för att iterera över alla kanter i samlingen.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Border>>> Aspose::Words::BorderCollection::GetEnumerator() override
```


## Exempel



Visar hur man itererar över och redigerar alla kanter i ett styckeformat-objekt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Konfigurera byggarens styckeformatinställningar för att skapa en grön vågkant på alla sidor.
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

// Infoga ett stycke. Våra kantinställningar kommer att bestämma hur dess kant ser ut.
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"BorderCollection.GetBordersEnumerator.docx");
```

## Se även

* Class [Border](../../border/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
