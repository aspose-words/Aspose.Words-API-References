---
title: "Aspose::Words::Lists::ListLevel class"
linktitle: "ListLevel"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Lists::ListLevel Klasse. Definiert die Formatierung für eine Listenebene. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.lists/listlevel/
---
## ListLevel class


Definiert die Formatierung für eine Listenebene. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class ListLevel : public Aspose::Words::IRunAttrSource
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [CreatePictureBullet](./createpicturebullet/)() | Erstellt das Bildaufzählungszeichen für die aktuelle Listenebene. |
| [DeletePictureBullet](./deletepicturebullet/)() | Löscht das Bildaufzählungszeichen für die aktuelle Listenebene. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Lists::ListLevel\>\&) | Vergleicht mit dem angegebenen [ListLevel](./). |
| [get_Alignment](./get_alignment/)() const | Liest oder setzt die Ausrichtung der tatsächlichen Nummer des Listenelements. |
| [get_CustomNumberStyleFormat](./get_customnumberstyleformat/)() | Liest oder setzt das benutzerdefinierte Zahlenstilformat für diese Listenebene. Zum Beispiel: "a, ç, ĝ, ...". |
| [get_Font](./get_font/)() | Gibt die Zeichenformatierung an, die für das Listensymbol verwendet wird. |
| [get_ImageData](./get_imagedata/)() | Gibt die Bilddaten des Bildaufzählungszeichens für die aktuelle Listenebene zurück. |
| [get_IsLegal](./get_islegal/)() const | True, wenn die Ebene alle vererbten Zahlen in Arabisch umwandelt, false, wenn sie ihren Zahlenstil beibehält. |
| [get_LinkedStyle](./get_linkedstyle/)() | Liest oder setzt den Absatzstil, der mit dieser Listenebene verknüpft ist. |
| [get_NumberFormat](./get_numberformat/)() const | Liefert oder setzt das Zahlenformat für die Listenebene. |
| [get_NumberPosition](./get_numberposition/)() const | Liefert oder setzt die Position (in Punkten) der Nummer oder des Aufzählungszeichens für die Listenebene. |
| [get_NumberStyle](./get_numberstyle/)() const | Liefert oder setzt den Zahlenstil für diese Listenebene. |
| [get_RestartAfterLevel](./get_restartafterlevel/)() const | Setzt oder liefert die Listenebene, die vor der angegebenen Listenebene erscheinen muss, um die Nummerierung neu zu starten. |
| [get_StartAt](./get_startat/)() | Liefert oder setzt die Startnummer für diese Listenebene. |
| [get_TabPosition](./get_tabposition/)() const | Liefert oder setzt die Tabulatorposition (in Punkten) für die Listenebene. |
| [get_TextPosition](./get_textposition/)() const | Liefert oder setzt die Position (in Punkten) für die zweite Zeile des umfließenden Textes der Listenebene. |
| [get_TrailingCharacter](./get_trailingcharacter/)() const | Liefert oder setzt das Zeichen, das nach der Nummer für die Listenebene eingefügt wird. |
| static [GetEffectiveValue](./geteffectivevalue/)(int32_t, Aspose::Words::NumberStyle, const System::String\&) | Gibt die Zeichenkettenrepräsentation des [ListLevel](./)-Objekts für den angegebenen Index des Listenelements zurück. Die Parameter geben den [NumberStyle](../../aspose.words/numberstyle/) und eine optionale Formatzeichenfolge an, die verwendet wird, wenn [Custom](../../aspose.words/numberstyle/) angegeben ist. |
| [GetHashCode](./gethashcode/)() const override | Berechnet den Hashcode für dieses Objekt. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveTabStop](./removetabstop/)() | Entfernt den Tabstopp von der Listenebene. |
| [set_Alignment](./set_alignment/)(Aspose::Words::Lists::ListLevelAlignment) | Setter für [Aspose::Words::Lists::ListLevel::get_Alignment](./get_alignment/). |
| [set_CustomNumberStyleFormat](./set_customnumberstyleformat/)(const System::String\&) | Setter für [Aspose::Words::Lists::ListLevel::get_CustomNumberStyleFormat](./get_customnumberstyleformat/). |
| [set_IsLegal](./set_islegal/)(bool) | Setter für [Aspose::Words::Lists::ListLevel::get_IsLegal](./get_islegal/). |
| [set_LinkedStyle](./set_linkedstyle/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Setter für [Aspose::Words::Lists::ListLevel::get_LinkedStyle](./get_linkedstyle/). |
| [set_NumberFormat](./set_numberformat/)(const System::String\&) | Setter für [Aspose::Words::Lists::ListLevel::get_NumberFormat](./get_numberformat/). |
| [set_NumberPosition](./set_numberposition/)(double) | Setter für [Aspose::Words::Lists::ListLevel::get_NumberPosition](./get_numberposition/). |
| [set_NumberStyle](./set_numberstyle/)(Aspose::Words::NumberStyle) | Setter für [Aspose::Words::Lists::ListLevel::get_NumberStyle](./get_numberstyle/). |
| [set_RestartAfterLevel](./set_restartafterlevel/)(int32_t) | Setter für [Aspose::Words::Lists::ListLevel::get_RestartAfterLevel](./get_restartafterlevel/). |
| [set_StartAt](./set_startat/)(int32_t) | Setter für [Aspose::Words::Lists::ListLevel::get_StartAt](./get_startat/). |
| [set_TabPosition](./set_tabposition/)(double) | Setter für [Aspose::Words::Lists::ListLevel::get_TabPosition](./get_tabposition/). |
| [set_TextPosition](./set_textposition/)(double) | Setter für [Aspose::Words::Lists::ListLevel::get_TextPosition](./get_textposition/). |
| [set_TrailingCharacter](./set_trailingcharacter/)(Aspose::Words::Lists::ListTrailingCharacter) | Setter für [Aspose::Words::Lists::ListLevel::get_TrailingCharacter](./get_trailingcharacter/). |
| static [Type](./type/)() |  |
## Hinweise


Sie erstellen keine Objekte dieser Klasse. [List](../list/) Ebenenobjekte werden automatisch erstellt, wenn eine Liste erstellt wird. Sie greifen über die Sammlung [ListLevelCollection](../listlevelcollection/) auf [ListLevel](./) Objekte zu.

Verwenden Sie die Eigenschaften von [ListLevel](./), um die Listformatierung für einzelne Listenebenen festzulegen.

## Beispiele



Zeigt, wie benutzerdefinierte Listformatierung auf Absätze angewendet wird, wenn [DocumentBuilder](../../aspose.words/documentbuilder/) verwendet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Eine Liste ermöglicht es uns, Absatzgruppen mit Präfixsymbolen und Einzügen zu organisieren und zu formatieren.
// Wir können verschachtelte Listen erstellen, indem wir die Einzugsebene erhöhen.
// Wir können eine Liste beginnen und beenden, indem wir die "ListFormat"-Eigenschaft eines Document Builders verwenden.
// Jeder Absatz, den wir zwischen dem Beginn und dem Ende einer Liste einfügen, wird zu einem Element in der Liste.
// Erstellen Sie eine Liste aus einer Microsoft‑Word‑Vorlage und passen Sie die ersten beiden Ebenen der Liste an.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = list->get_ListLevels()->idx_get(0);
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Red());
listLevel->get_Font()->set_Size(24);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::OrdinalText);
listLevel->set_StartAt(21);
listLevel->set_NumberFormat(u"\x0000");

listLevel->set_NumberPosition(-36);
listLevel->set_TextPosition(144);
listLevel->set_TabPosition(144);

listLevel = list->get_ListLevels()->idx_get(1);
listLevel->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::Bullet);
listLevel->get_Font()->set_Name(u"Wingdings");
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Blue());
listLevel->get_Font()->set_Size(24);

// Dieser NumberFormat‑Wert erzeugt sternförmige Aufzählungszeichen.
listLevel->set_NumberFormat(u"\xf0af");
listLevel->set_TrailingCharacter(Aspose::Words::Lists::ListTrailingCharacter::Space);
listLevel->set_NumberPosition(144);

// Erstellen Sie Absätze und wenden Sie beide Listenebenen unserer benutzerdefinierten Listformatierung darauf an.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->set_List(list);
builder->Writeln(u"The quick brown fox...");
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->ListIndent();
builder->Writeln(u"jumped over the lazy dog.");
builder->Writeln(u"jumped over the lazy dog.");

builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateCustomList.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
