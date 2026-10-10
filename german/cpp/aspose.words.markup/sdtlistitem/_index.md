---
title: "Aspose::Words::Markup::SdtListItem Klasse"
linktitle: "SdtListItem"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::SdtListItem Klasse. Dieses Element gibt ein einzelnes Listenelement innerhalb eines übergeordneten ComboBox- oder DropDownList-Strukturierten Dokument-Tags an. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 8000
url: /de/cpp/aspose.words.markup/sdtlistitem/
---
## SdtListItem class


Dieses Element gibt ein einzelnes Listenelement innerhalb eines übergeordneten [ComboBox](../sdttype/) oder [DropDownList](../sdttype/) strukturierten Dokumenttags an. Weitere Informationen finden Sie im Dokumentationsartikel [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class SdtListItem : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_DisplayText](./get_displaytext/)() const | Liefert den Text, der im Laufinhalt anstelle des Attributinhalts [Value](./get_value/) für dieses Listenelement angezeigt wird. |
| [get_Value](./get_value/)() const | Liefert den Wert dieses Listenelements. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [SdtListItem](./sdtlistitem/)(const System::String\&, const System::String\&) | Initialisiert eine neue Instanz dieser Klasse. |
| [SdtListItem](./sdtlistitem/)(const System::String\&) | Initialisiert eine neue Instanz dieser Klasse. |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man mit Drop‑Down‑Listen‑Strukturierten‑Dokumenttags arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::DropDownList, Aspose::Words::Markup::MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

// Ein Drop‑Down‑Listen‑Struktur‑Dokumenttag ist ein Formular, das dem Benutzer ermöglicht,
// eine Option aus einer Liste durch Links‑Klick auszuwählen und das Formular in Microsoft Word zu öffnen.
// Die Eigenschaft "ListItems" enthält alle Listenelemente, und jedes Listenelement ist ein "SdtListItem".
System::SharedPtr<Aspose::Words::Markup::SdtListItemCollection> listItems = tag->get_ListItems();
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Value 1"));

ASSERT_EQ(listItems->idx_get(0)->get_DisplayText(), listItems->idx_get(0)->get_Value());

// Fügen Sie 3 weitere Listenelemente hinzu. Initialisieren Sie diese Elemente mit einem anderen Konstruktor als das erste Element
// um Zeichenketten anzuzeigen, die sich von ihren Werten unterscheiden.
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 2", u"Value 2"));
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 3", u"Value 3"));
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 4", u"Value 4"));

ASSERT_EQ(4, listItems->get_Count());

// Die Drop‑Down‑Liste zeigt das erste Element an. Weisen Sie ein anderes Listenelement der "SelectedValue" zu, um es anzuzeigen.
listItems->set_SelectedValue(listItems->idx_get(3));

ASSERT_EQ(u"Value 4", listItems->get_SelectedValue()->get_Value());

// Durchlaufen Sie die Sammlung und geben Sie jedes Element aus.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::SdtListItem>>> enumerator = listItems->GetEnumerator();
    while (enumerator->MoveNext())
    {
        if (enumerator->get_Current() != nullptr)
        {
            std::cout << System::String::Format(u"List item: {0}, value: {1}", enumerator->get_Current()->get_DisplayText(), enumerator->get_Current()->get_Value()) << std::endl;
        }
    }
}

// Entfernen Sie das letzte Listenelement.
listItems->RemoveAt(3);

ASSERT_EQ(3, listItems->get_Count());

// Da unser Drop‑Down‑Steuerelement standardmäßig das entfernte Element anzeigt, geben Sie ihm ein vorhandenes Element zum Anzeigen.
listItems->set_SelectedValue(listItems->idx_get(1));

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.ListItemCollection.docx");

// Verwenden Sie die Methode "Clear", um die gesamte Drop‑Down‑Elementsammlung auf einmal zu leeren.
listItems->Clear();

ASSERT_EQ(0, listItems->get_Count());
```

## Siehe auch

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
