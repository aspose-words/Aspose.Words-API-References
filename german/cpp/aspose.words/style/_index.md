---
title: "Aspose::Words::Style class"
linktitle: "Style"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Style class. Stellt einen einzelnen integrierten oder benutzerdefinierten Stil dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 64000
url: /de/cpp/aspose.words/style/
---
## Style class


Stellt einen einzelnen integrierten oder benutzerdefinierten Stil dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/).

```cpp
class Style : public Aspose::Words::IParaAttrSource,
              public Aspose::Words::IRunAttrSource
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Vergleicht mit dem angegebenen Stil. Stil‑IDs werden nur für integrierte Stile verglichen. Standard‑Stile sind im Vergleich nicht enthalten. Basisstil, verknüpfter Stil und nächster Absatzstil werden rekursiv verglichen. |
| [get_Aliases](./get_aliases/)() | Ruft alle Aliase dieses Stils ab. Wenn der Stil keine Aliase hat, wird ein leeres String‑Array zurückgegeben. |
| [get_AutomaticallyUpdate](./get_automaticallyupdate/)() const | Gibt an, ob dieser Stil basierend auf dem entsprechenden Wert automatisch neu definiert wird. |
| [get_BaseStyleName](./get_basestylename/)() | Ruft den Namen des Stils ab bzw. legt ihn fest, auf dem dieser Stil basiert. |
| [get_BuiltIn](./get_builtin/)() | Wahr, wenn dieser Stil einer der integrierten Stile in MS Word ist. |
| [get_Document](./get_document/)() | Ermittelt das übergeordnete Dokument. |
| [get_Font](./get_font/)() | Ruft die Zeichenformatierung des Stils ab. |
| [get_IsHeading](./get_isheading/)() | Wahr, wenn der Stil einer der integrierten Überschrifts‑Stile ist. |
| [get_IsQuickStyle](./get_isquickstyle/)() const | Gibt an, ob dieser Stil in der Schnell-[Style](./)-Galerie in der MS‑Word‑Benutzeroberfläche angezeigt wird. |
| [get_LinkedStyleName](./get_linkedstylename/)() | Ruft den Namen des mit diesem verknüpften [Style](./) ab bzw. legt ihn fest. Gibt einen leeren String zurück, wenn keine Stile verknüpft sind. |
| [get_List](./get_list/)() | Ruft die Liste ab, die die Formatierung dieses Listenstils definiert. |
| [get_ListFormat](./get_listformat/)() | Bietet Zugriff auf die Listformatierungseigenschaften eines Absatzstils. |
| [get_Locked](./get_locked/)() const | Gibt an, ob dieser Stil gesperrt ist. |
| [get_Name](./get_name/)() const | Ruft den Namen des Stils ab bzw. legt ihn fest. |
| [get_NextParagraphStyleName](./get_nextparagraphstylename/)() | Liest/Setzt den Namen des Stils, der automatisch auf einen neuen Absatz angewendet wird, der nach einem mit dem angegebenen Stil formatierten Absatz eingefügt wird. |
| [get_ParagraphFormat](./get_paragraphformat/)() | Liest die Absatzformatierung des Stils. |
| [get_Priority](./get_priority/)() const | Liest/Setzt den ganzzahligen Wert, der die Priorität für die Sortierung der Stile im Aufgabenbereich Stile darstellt. |
| [get_SemiHidden](./get_semihidden/)() const | Liest/Setzt, ob der Stil in der Stile-Galerie und im Aufgabenbereich Stile ausgeblendet wird. |
| [get_StyleIdentifier](./get_styleidentifier/)() const | Liest den sprachunabhängigen Stilbezeichner für einen integrierten Stil. |
| [get_Styles](./get_styles/)() const | Liest die Sammlung von Stilen, zu denen dieser Stil gehört. |
| [get_Type](./get_type/)() const | Liest den Stiltyp (Absatz oder Zeichen). |
| [get_UnhideWhenUsed](./get_unhidewhenused/)() const | Liest/Setzt, ob der im aktuellen Dokument verwendete Stil in der Stile-Galerie und im Aufgabenbereich Stile wieder eingeblendet wird. Wahr, wenn der verwendete Stil in der Stile-Galerie angezeigt werden soll. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Entfernt den angegebenen Stil aus dem Dokument. |
| [set_AutomaticallyUpdate](./set_automaticallyupdate/)(bool) | Setter für [Aspose::Words::Style::get_AutomaticallyUpdate](./get_automaticallyupdate/). |
| [set_BaseStyleName](./set_basestylename/)(const System::String\&) | Setter für [Aspose::Words::Style::get_BaseStyleName](./get_basestylename/). |
| [set_IsQuickStyle](./set_isquickstyle/)(bool) | Setter für [Aspose::Words::Style::get_IsQuickStyle](./get_isquickstyle/). |
| [set_LinkedStyleName](./set_linkedstylename/)(const System::String\&) | Setter für [Aspose::Words::Style::get_LinkedStyleName](./get_linkedstylename/). |
| [set_Locked](./set_locked/)(bool) | Setter für [Aspose::Words::Style::get_Locked](./get_locked/). |
| [set_Name](./set_name/)(const System::String\&) | Setter für [Aspose::Words::Style::get_Name](./get_name/). |
| [set_NextParagraphStyleName](./set_nextparagraphstylename/)(const System::String\&) | Setter für [Aspose::Words::Style::get_NextParagraphStyleName](./get_nextparagraphstylename/). |
| [set_Priority](./set_priority/)(int32_t) | Setter für [Aspose::Words::Style::get_Priority](./get_priority/). |
| [set_SemiHidden](./set_semihidden/)(bool) | Setter für [Aspose::Words::Style::get_SemiHidden](./get_semihidden/). |
| [set_UnhideWhenUsed](./set_unhidewhenused/)(bool) | Setter für [Aspose::Words::Style::get_UnhideWhenUsed](./get_unhidewhenused/). |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man einen benutzerdefinierten Stil erstellt und anwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
style->get_Font()->set_Name(u"Times New Roman");
style->get_Font()->set_Size(16);
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());
// Stil automatisch neu definieren.
style->set_AutomaticallyUpdate(true);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Wendet einen der Stile aus dem Dokument auf den Absatz an, den der Dokumenten-Builder erstellt.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Style> firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

ASPOSE_ASSERT_EQ(style, firstParagraphStyle);

// Entfernt unseren benutzerdefinierten Stil aus der Stilsammlung des Dokuments.
doc->get_Styles()->idx_get(u"MyStyle")->Remove();

firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

// Jeglicher Text, der einen entfernten Stil verwendet hat, wird zur Standardformatierung zurückkehren.
ASSERT_FALSE(doc->get_Styles()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Style>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Style> s)>>([](System::SharedPtr<Aspose::Words::Style> s) -> bool
{
    return s->get_Name() == u"MyStyle";
}))));
ASSERT_EQ(u"Times New Roman", firstParagraphStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(12.0, firstParagraphStyle->get_Font()->get_Size());
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), firstParagraphStyle->get_Font()->get_Color().ToArgb());
```


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
