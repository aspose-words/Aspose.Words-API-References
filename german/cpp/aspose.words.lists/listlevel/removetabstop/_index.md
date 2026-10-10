---
title: "Aspose::Words::Lists::ListLevel::RemoveTabStop Methode"
linktitle: "RemoveTabStop"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Lists::ListLevel::RemoveTabStop Methode. Entfernt den Tabstop vom ListLevel in C++."
type: docs
weight: 22500
url: /de/cpp/aspose.words.lists/listlevel/removetabstop/
---
## ListLevel::RemoveTabStop method


Entfernt den Tabstopp von der Listenebene.

```cpp
void Aspose::Words::Lists::ListLevel::RemoveTabStop()
```


## Beispiele



Zeigt, wie man den Tabstop des ListLevels löscht.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Erstelle eine Liste mit Standardformatierung
builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Numbered list item 1");
builder->Writeln(u"Numbered list item 2");

// Hole das ListLevel und entferne dessen Tabstop
System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = builder->get_ListFormat()->get_ListLevel();
listLevel->RemoveTabStop();

doc->Save(get_ArtifactsDir() + u"Paragraph.RemoveTabStopFromListLevel.docx");
```

## Siehe auch

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
