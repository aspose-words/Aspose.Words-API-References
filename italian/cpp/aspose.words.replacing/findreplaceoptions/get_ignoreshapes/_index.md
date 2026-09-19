---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreShapes method"
linktitle: "get_IgnoreShapes"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreShapes method. Ottiene o imposta un valore booleano che indica se ignorare le forme all'interno di un testo. Il valore predefinito è false in C++."
type: docs
weight: 11500
url: /it/cpp/aspose.words.replacing/findreplaceoptions/get_ignoreshapes/
---
## FindReplaceOptions::get_IgnoreShapes method


Ottiene o imposta un valore booleano che indica se ignorare le forme all'interno di un testo. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreShapes() const
```


## Esempi



Mostra come ignorare le forme durante la sostituzione del testo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Balloon, 200, 200);
builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

auto findReplaceOptions = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
findReplaceOptions->set_IgnoreShapes(true);
builder->get_Document()->get_Range()->Replace(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.Lorem ipsum dolor sit amet, consectetur adipiscing elit.", u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.", findReplaceOptions);
ASSERT_EQ(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.", builder->get_Document()->GetText().Trim());
```

## Vedi anche

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
