---
title: GetEnumerator
second_title: Aspose.Words for C++ API Reference
description: Returns an enumerator object that can be used to iterate over all borders in the collection.
type: docs
weight: 183
url: /cpp/aspose.words/bordercollection/getenumerator/
---
## BorderCollection.GetEnumerator method


Returns an enumerator object that can be used to iterate over all borders in the collection.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Border>>> Aspose::Words::BorderCollection::GetEnumerator() override
```


## Examples




Shows how to iterate over and edit all of the borders in a paragraph format object. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Configure the builder's paragraph format settings to create a green wave border on all sides.
SharedPtr<BorderCollection> borders = builder->get_ParagraphFormat()->get_Borders();

{
    SharedPtr<System::Collections::Generic::IEnumerator<SharedPtr<Border>>> enumerator = borders->GetEnumerator();
    while (enumerator->MoveNext())
    {
        SharedPtr<Border> border = enumerator->get_Current();
        border->set_Color(System::Drawing::Color::get_Green());
        border->set_LineStyle(LineStyle::Wave);
        border->set_LineWidth(3);
    }
}

// Insert a paragraph. Our border settings will determine the appearance of its border.
builder->Writeln(u"Hello world!");

doc->Save(ArtifactsDir + u"BorderCollection.GetBordersEnumerator.docx");
```

