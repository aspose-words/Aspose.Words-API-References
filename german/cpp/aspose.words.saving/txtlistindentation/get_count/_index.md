---
title: "Aspose::Words::Saving::TxtListIndentation::get_Count-Methode"
linktitle: "get_Count"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::TxtListIndentation::get_Count-Methode. Gibt an, wie viele Zeichen als Einrückung pro Listenebene verwendet werden sollen, oder legt diesen Wert fest. Der Standardwert ist 0, was bedeutet, dass in C++ keine Einrückung erfolgt."
type: docs
weight: 4000
url: /de/cpp/aspose.words.saving/txtlistindentation/get_count/
---
## TxtListIndentation::get_Count method


Gibt an, wie viele [Character](../get_character/) als Einrückung pro Listenebene verwendet werden sollen, oder legt diesen Wert fest. Der Standardwert ist 0, was bedeutet, dass keine Einrückung erfolgt.

```cpp
int32_t Aspose::Words::Saving::TxtListIndentation::get_Count() const
```


## Beispiele



Zeigt, wie die Listeneinrückung beim Speichern eines Dokuments als Klartext konfiguriert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Erstellen Sie eine Liste mit drei Einrückungsebenen.
builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Item 1");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 2");
builder->get_ListFormat()->ListIndent();
builder->Write(u"Item 3");

// Erstelle ein "TxtSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie wir das Dokument in Klartext speichern.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Setzen Sie die Eigenschaft "Character", um ein zu verwendendes Zeichen zuzuweisen
// für die Auffüllung, die die Listeneinrückung im Klartext simuliert.
txtSaveOptions->get_ListIndentation()->set_Character(u' ');

// Setzen Sie die Eigenschaft "Count", um die Anzahl der Wiederholungen festzulegen
// um das Auffüllungszeichen für jede Listeneinrückungsebene zu platzieren.
txtSaveOptions->get_ListIndentation()->set_Count(3);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.TxtListIndentation.txt");
System::String newLine = System::Environment::get_NewLine();

ASSERT_EQ(System::String::Format(u"1. Item 1{0}", newLine) + System::String::Format(u"   a. Item 2{0}", newLine) + System::String::Format(u"      i. Item 3{0}", newLine), docText);
```

## Siehe auch

* Class [TxtListIndentation](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
