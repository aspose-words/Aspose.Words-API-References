---
title: "Aspose::Words::Fields::ToaCategories Klasse"
linktitle: "ToaCategories"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::ToaCategories Klasse. Stellt eine Tabelle von Autoritätskategorien dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 116000
url: /de/cpp/aspose.words.fields/toacategories/
---
## ToaCategories class


Stellt eine Tabelle von Kategorien für Autoritäten dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class ToaCategories : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| static [get_DefaultCategories](./get_defaultcategories/)() | Liefert die Standardtabelle der Autoritätskategorien. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Liefert oder setzt die Kategorienüberschrift anhand der Kategorienummer. |
| [idx_set](./idx_set/)(int32_t, const System::String\&) | Liefert oder setzt die Kategorienüberschrift anhand der Kategorienummer. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ToaCategories](./toacategories/)() |  |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie ein Satz von Kategorien für TOA-Felder angegeben wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// TOA-Felder können ihre Einträge nach Kategorien filtern, die in dieser Sammlung definiert sind.
auto toaCategories = System::MakeObject<Aspose::Words::Fields::ToaCategories>();
doc->get_FieldOptions()->set_ToaCategories(toaCategories);

// Diese Sammlung von Kategorien enthält Standardwerte, die wir mit benutzerdefinierten Werten überschreiben können.
ASSERT_EQ(u"Cases", toaCategories->idx_get(1));
ASSERT_EQ(u"Statutes", toaCategories->idx_get(2));

toaCategories->idx_set(1, u"My Category 1");
toaCategories->idx_set(2, u"My Category 2");

// Wir können jederzeit über diese Sammlung auf die Standardwerte zugreifen.
ASSERT_EQ(u"Cases", Aspose::Words::Fields::ToaCategories::get_DefaultCategories()->idx_get(1));
ASSERT_EQ(u"Statutes", Aspose::Words::Fields::ToaCategories::get_DefaultCategories()->idx_get(2));

// Fügen Sie 2 TOA-Felder ein. TOA-Felder erstellen einen Eintrag für jedes TA-Feld im Dokument.
// Verwenden Sie den Schalter "\c", um den Index einer Kategorie aus unserer Sammlung auszuwählen.
//  Mit diesem Schalter wird ein TOA-Feld nur Einträge von TA-Feldern übernehmen, die
// ebenfalls einen "\c"-Schalter mit einem passenden Kategorienindex haben. Jedes TOA-Feld wird außerdem anzeigen
// den Namen der Kategorie, auf die sein "\c"-Schalter verweist.
builder->InsertField(u"TOA \\c 1 \\h", nullptr);
builder->InsertField(u"TOA \\c 2 \\h", nullptr);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Fügen Sie TOA-Einträge über 2 Kategorien ein. Unser erstes TOA-Feld wird einen Eintrag erhalten,
// aus dem zweiten TA-Feld, dessen "\c"-Schalter ebenfalls auf die erste Kategorie zeigt.
// Das zweite TOA-Feld wird zwei Einträge von den anderen beiden TA-Feldern haben.
builder->InsertField(u"TA \\c 2 \\l \"entry 1\"");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertField(u"TA \\c 1 \\l \"entry 2\"");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertField(u"TA \\c 2 \\l \"entry 3\"");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.TOA.Categories.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
