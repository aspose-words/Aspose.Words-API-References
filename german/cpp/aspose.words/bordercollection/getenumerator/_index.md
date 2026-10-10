---
title: "Aspose::Words::BorderCollection::GetEnumerator Methode"
linktitle: "GetEnumerator"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::BorderCollection::GetEnumerator Methode. Gibt ein Enumerator‑Objekt zurück, das verwendet werden kann, um über alle Ränder in der Sammlung in C++ zu iterieren."
type: docs
weight: 16000
url: /de/cpp/aspose.words/bordercollection/getenumerator/
---
## BorderCollection::GetEnumerator method


Gibt ein Enumerator-Objekt zurück, das verwendet werden kann, um über alle Rahmen in der Sammlung zu iterieren.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Border>>> Aspose::Words::BorderCollection::GetEnumerator() override
```


## Beispiele



Zeigt, wie man über alle Ränder in einem Absatzformat‑Objekt iteriert und sie bearbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Konfigurieren Sie die Absatzformat‑Einstellungen des Builders, um einen grünen Wellenrand an allen Seiten zu erstellen.
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

// Fügen Sie einen Absatz ein. Unsere Rand‑Einstellungen bestimmen das Aussehen seines Randes.
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"BorderCollection.GetBordersEnumerator.docx");
```

## Siehe auch

* Class [Border](../../border/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
