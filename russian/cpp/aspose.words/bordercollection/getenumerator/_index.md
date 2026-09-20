---
title: "Aspose::Words::BorderCollection::GetEnumerator method"
linktitle: "GetEnumerator"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::BorderCollection::GetEnumerator. Возвращает объект‑перечислитель, который можно использовать для перебора всех границ в коллекции в C++."
type: docs
weight: 16000
url: /ru/cpp/aspose.words/bordercollection/getenumerator/
---
## BorderCollection::GetEnumerator method


Возвращает объект‑перечислитель, который можно использовать для перебора всех границ в коллекции.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Border>>> Aspose::Words::BorderCollection::GetEnumerator() override
```


## Примеры



Показано, как перебрать и изменить все границы в объекте формата абзаца.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Настройте параметры формата абзаца построителя, чтобы создать зелёную волнистую границу со всех сторон.
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

// Вставьте абзац. Наши настройки границы определят её внешний вид.
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"BorderCollection.GetBordersEnumerator.docx");
```

## См. также

* Class [Border](../../border/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
