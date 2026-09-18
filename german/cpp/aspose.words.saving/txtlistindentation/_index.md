---
title: "Aspose::Words::Saving::TxtListIndentation Klasse"
linktitle: "TxtListIndentation"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::TxtListIndentation Klasse. Gibt an, wie Listenebenen eingerückt werden, wenn das Dokument in das Textformat exportiert wird. Weitere Informationen finden Sie im Dokumentationsartikel in C++."
type: docs
weight: 32000
url: /de/cpp/aspose.words.saving/txtlistindentation/
---
## TxtListIndentation class


Gibt an, wie Listenebenen eingerückt werden, wenn das Dokument in das [Text](../../aspose.words/saveformat/) Format exportiert wird. Weitere Informationen finden Sie im Dokumentationsartikel [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class TxtListIndentation : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Character](./get_character/)() const | Liest oder legt das Zeichen fest, das zum Einrücken von Listenebenen verwendet wird. Der Standardwert ist '\0', das bedeutet, dass keine Einrückung vorhanden ist. |
| [get_Count](./get_count/)() const | Liest oder legt fest, wie viele [Character](./get_character/) als Einrückung pro Listenebene verwendet werden. Der Standardwert ist 0, das bedeutet keine Einrückung. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Character](./set_character/)(char16_t) | Setter für [Aspose::Words::Saving::TxtListIndentation::get_Character](./get_character/). |
| [set_Count](./set_count/)(int32_t) | Setter für [Aspose::Words::Saving::TxtListIndentation::get_Count](./get_count/). |
| [TxtListIndentation](./txtlistindentation/)() |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
