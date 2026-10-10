---
title: "Aspose::Words::Drawing::OleFormat::get_SuggestedFileName Methode"
linktitle: "get_SuggestedFileName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::OleFormat::get_SuggestedFileName Methode. Gibt den für das aktuelle eingebettete Objekt vorgeschlagenen Dateinamen zurück, wenn Sie ihn in C++ in einer Datei speichern möchten."
type: docs
weight: 14000
url: /de/cpp/aspose.words.drawing/oleformat/get_suggestedfilename/
---
## OleFormat::get_SuggestedFileName method


Liest den für das aktuelle eingebettete Objekt empfohlenen Dateinamen, wenn Sie es in einer Datei speichern möchten.

```cpp
System::String Aspose::Words::Drawing::OleFormat::get_SuggestedFileName()
```


## Beispiele



Zeigt, wie man den vorgeschlagenen Dateinamen eines OLE-Objekts erhält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE shape.rtf");

auto oleShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->get_FirstSection()->get_Body()->GetChild(Aspose::Words::NodeType::Shape, 0, true));

// OLE-Objekte können einen vorgeschlagenen Dateinamen und eine Erweiterung bereitstellen,
// die wir beim Speichern des Objektinhalts in einer Datei im lokalen Dateisystem verwenden können.
System::String suggestedFileName = oleShape->get_OleFormat()->get_SuggestedFileName();

ASSERT_EQ(u"CSV.csv", suggestedFileName);

{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + suggestedFileName, System::IO::FileMode::Create);
    oleShape->get_OleFormat()->Save(fileStream);
}
```

## Siehe auch

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
