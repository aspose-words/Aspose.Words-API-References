---
title: "Aspose::Words::StyleCollection::idx_get Methode"
linktitle: "idx_get"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::StyleCollection::idx_get Methode. Ruft einen integrierten Stil anhand seiner sprachunabhängigen Kennung in C++ ab."
type: docs
weight: 11000
url: /de/cpp/aspose.words/stylecollection/idx_get/
---
## StyleCollection::idx_get(Aspose::Words::StyleIdentifier) method


Ermittelt einen integrierten Stil anhand seines lokalunabhängigen Bezeichners.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::idx_get(Aspose::Words::StyleIdentifier sti)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sti | Aspose::Words::StyleIdentifier | Ein [StyleIdentifier](../../styleidentifier/)-Wert, der den abzurufenden integrierten Stil angibt. |
## Hinweise


Beim Zugriff auf einen Stil, der noch nicht existiert, wird er automatisch erstellt.

## Beispiele



Zeigt, wie ein [Style](../../style/) zur Stilsammlung eines Dokuments hinzugefügt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// Legen Sie Standardparameter für neue Stile fest, die wir später zu dieser Sammlung hinzufügen können.
styles->get_DefaultFont()->set_Name(u"Courier New");
// Wenn wir einen Stil vom Typ \"StyleType.Paragraph\" hinzufügen, wendet die Sammlung die Werte von
// seiner \"DefaultParagraphFormat\"-Eigenschaft auf die \"ParagraphFormat\"-Eigenschaft des Stils an.
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// Fügen Sie einen Stil hinzu und überprüfen Sie anschließend, ob er die Standardeinstellungen hat.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## Siehe auch

* Class [Style](../../style/)
* Enum [StyleIdentifier](../../styleidentifier/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## StyleCollection::idx_get(const System::String\&) method


Ermittelt einen Stil anhand seines Namens oder Alias.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::idx_get(const System::String &name)
```

## Hinweise


Groß-/Kleinschreibung beachten, gibt **null** zurück, wenn der Stil mit dem angegebenen Namen nicht gefunden wird.

Wenn dies ein englischer Name eines integrierten Stils ist, der noch nicht existiert, wird er automatisch erstellt.

## Beispiele



Zeigt, wann das Seitenlayout des Dokuments neu berechnet werden muss.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Das Speichern eines Dokuments als PDF, als Bild oder das erstmalige Drucken wird automatisch
// Cache das Layout des Dokuments innerhalb seiner Seiten.
doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.1.pdf");

// Das Dokument auf irgendeine Weise ändern.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(6);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Margins(Aspose::Words::Margins::Mirrored);

// In der aktuellen Version von Aspose.Words wird das Dokument beim Ändern nicht automatisch neu aufgebaut
// das zwischengespeicherte Seitenlayout. Wenn wir möchten, dass das zwischengespeicherte Layout
// auf dem neuesten Stand bleibt, müssen wir es manuell aktualisieren.
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.2.pdf");
```

## Siehe auch

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## StyleCollection::idx_get(int32_t) method


Ermittelt einen Stil anhand seines Index.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::idx_get(int32_t index)
```


## Beispiele



Zeigt, wie ein [Style](../../style/) zur Stilsammlung eines Dokuments hinzugefügt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// Legen Sie Standardparameter für neue Stile fest, die wir später zu dieser Sammlung hinzufügen können.
styles->get_DefaultFont()->set_Name(u"Courier New");
// Wenn wir einen Stil vom Typ \"StyleType.Paragraph\" hinzufügen, wendet die Sammlung die Werte von
// seiner \"DefaultParagraphFormat\"-Eigenschaft auf die \"ParagraphFormat\"-Eigenschaft des Stils an.
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// Fügen Sie einen Stil hinzu und überprüfen Sie anschließend, ob er die Standardeinstellungen hat.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## Siehe auch

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
