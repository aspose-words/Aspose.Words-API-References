---
title: "Aspose::Words::StyleCollection Klasse"
linktitle: "StyleCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::StyleCollection Klasse. Eine Sammlung von Style-Objekten, die sowohl die integrierten als auch benutzerdefinierten Stile in einem Dokument darstellen. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 65000
url: /de/cpp/aspose.words/stylecollection/
---
## StyleCollection class


Eine Sammlung von [Style](../style/)-Objekten, die sowohl die integrierten als auch benutzerdefinierten Stile in einem Dokument darstellen. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/).

```cpp
class StyleCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Style>>
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Add](./add/)(Aspose::Words::StyleType, const System::String\&) | Erstellt einen neuen benutzerdefinierten Stil und fügt ihn der Sammlung hinzu. |
| [AddCopy](./addcopy/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Kopiert einen Stil in diese Sammlung. |
| [ClearQuickStyleGallery](./clearquickstylegallery/)() | Entfernt alle Stile aus dem Schnell-[Style](../style/)-Galerie‑Panel. |
| [get_Count](./get_count/)() | Ermittelt die Anzahl der Stile in der Sammlung. |
| [get_DefaultFont](./get_defaultfont/)() | Ermittelt die standardmäßige Textformatierung des Dokuments. |
| [get_DefaultParagraphFormat](./get_defaultparagraphformat/)() | Ermittelt die standardmäßige Absatzformatierung des Dokuments. |
| [get_Document](./get_document/)() const | Ermittelt das übergeordnete Dokument. |
| [GetEnumerator](./getenumerator/)() override | Gibt ein Enumerator‑Objekt zurück, das die Stile in alphabetischer Reihenfolge ihrer Namen aufzählt. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Ermittelt einen Stil anhand seines Namens oder Alias. |
| [idx_get](./idx_get/)(Aspose::Words::StyleIdentifier) | Ermittelt einen integrierten Stil anhand seines lokalunabhängigen Bezeichners. |
| [idx_get](./idx_get/)(int32_t) | Ermittelt einen Stil anhand seines Index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man einen Absatzstil mit Listformatierung erstellt und verwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Erstelle einen benutzerdefinierten Absatzstil.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// Erstelle eine Liste und stelle sicher, dass die Absätze, die diesen Stil verwenden, diese Liste verwenden.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// Wende den Absatzstil auf den aktuellen Absatz des DocumentBuilder an und füge dann etwas Text hinzu.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// Ändere den Stil des DocumentBuilder zu einem, das keine Listformatierung hat, und schreibe einen weiteren Absatz.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
