---
title: "Aspose::Words::Drawing::OleFormat::get_SuggestedFileName metod"
linktitle: "get_SuggestedFileName"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::OleFormat::get_SuggestedFileName metod. Hämtar det föreslagna filnamnet för det aktuella inbäddade objektet om du vill spara det i en fil i C++."
type: docs
weight: 14000
url: /sv/cpp/aspose.words.drawing/oleformat/get_suggestedfilename/
---
## OleFormat::get_SuggestedFileName method


Hämtar filnamnet som föreslås för det aktuella inbäddade objektet om du vill spara det i en fil.

```cpp
System::String Aspose::Words::Drawing::OleFormat::get_SuggestedFileName()
```


## Exempel



Visar hur man får ett OLE-objekts föreslagna filnamn.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE shape.rtf");

auto oleShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->get_FirstSection()->get_Body()->GetChild(Aspose::Words::NodeType::Shape, 0, true));

// OLE-objekt kan tillhandahålla ett föreslaget filnamn och filändelse,
// vilket vi kan använda när vi sparar objektets innehåll i en fil i det lokala filsystemet.
System::String suggestedFileName = oleShape->get_OleFormat()->get_SuggestedFileName();

ASSERT_EQ(u"CSV.csv", suggestedFileName);

{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + suggestedFileName, System::IO::FileMode::Create);
    oleShape->get_OleFormat()->Save(fileStream);
}
```

## Se även

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
