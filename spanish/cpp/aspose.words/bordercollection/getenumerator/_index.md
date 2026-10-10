---
title: "Aspose::Words::BorderCollection::GetEnumerator método"
linktitle: "GetEnumerator"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::BorderCollection::GetEnumerator. Devuelve un objeto enumerador que puede usarse para iterar sobre todos los bordes de la colección en C++."
type: docs
weight: 16000
url: /es/cpp/aspose.words/bordercollection/getenumerator/
---
## BorderCollection::GetEnumerator method


Devuelve un objeto enumerador que puede usarse para iterar sobre todos los bordes de la colección.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Border>>> Aspose::Words::BorderCollection::GetEnumerator() override
```


## Ejemplos



Muestra cómo iterar y editar todos los bordes en un objeto de formato de párrafo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Configure los ajustes de formato de párrafo del constructor para crear un borde de onda verde en todos los lados.
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

// Inserte un párrafo. Nuestra configuración de bordes determinará la apariencia de su borde.
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"BorderCollection.GetBordersEnumerator.docx");
```

## Ver también

* Class [Border](../../border/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
