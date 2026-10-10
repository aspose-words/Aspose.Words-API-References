---
title: "Aspose::Words::Lists::ListLevel::RemoveTabStop‑metod"
linktitle: "RemoveTabStop"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Lists::ListLevel::RemoveTabStop‑metod. Tar bort tabbstopp från listnivån i C++."
type: docs
weight: 22500
url: /sv/cpp/aspose.words.lists/listlevel/removetabstop/
---
## ListLevel::RemoveTabStop method


Tar bort tabbstopp från listnivån.

```cpp
void Aspose::Words::Lists::ListLevel::RemoveTabStop()
```


## Exempel



Visar hur man rensar tabbstoppet för listnivån.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Skapa en lista med standardformatering
builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Numbered list item 1");
builder->Writeln(u"Numbered list item 2");

// Hämta listnivån och ta bort dess tabbstopp
System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = builder->get_ListFormat()->get_ListLevel();
listLevel->RemoveTabStop();

doc->Save(get_ArtifactsDir() + u"Paragraph.RemoveTabStopFromListLevel.docx");
```

## Se även

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
