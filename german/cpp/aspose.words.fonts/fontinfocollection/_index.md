---
title: "Aspose::Words::Fonts::FontInfoCollection class"
linktitle: "FontInfoCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FontInfoCollection Klasse. Stellt eine Sammlung von Schriftarten dar, die in einem Dokument verwendet werden. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 7000
url: /de/cpp/aspose.words.fonts/fontinfocollection/
---
## FontInfoCollection class


Stellt eine Sammlung von im Dokument verwendeten Schriftarten dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontInfoCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fonts::FontInfo>>
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Contains](./contains/)(const System::String\&) | Bestimmt, ob die Sammlung eine Schriftart mit dem angegebenen Namen enthält. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Gibt die Anzahl der in der Sammlung enthaltenen Elemente zurück. |
| [get_EmbedSystemFonts](./get_embedsystemfonts/)() const | Gibt an, ob Systemschriftarten in das Dokument eingebettet werden sollen oder nicht. Der Standardwert für diese Eigenschaft ist **false**. Diese Option funktioniert nur, wenn die [EmbedTrueTypeFonts](./get_embedtruetypefonts/) Option auf **true** gesetzt ist. |
| [get_EmbedTrueTypeFonts](./get_embedtruetypefonts/)() const | Gibt an, ob TrueType‑Schriftarten beim Speichern eines Dokuments eingebettet werden sollen oder nicht. Der Standardwert für diese Eigenschaft ist **false**. |
| [get_SaveSubsetFonts](./get_savesubsetfonts/)() const | Gibt an, ob ein Teil der eingebetteten TrueType‑Schriftarten mit dem Dokument gespeichert werden soll oder nicht. Der Standardwert für diese Eigenschaft ist **false**. Diese Option funktioniert nur, wenn die [EmbedTrueTypeFonts](./get_embedtruetypefonts/) Eigenschaft auf **true** gesetzt ist. |
| [GetEnumerator](./getenumerator/)() override | Gibt ein Enumerator‑Objekt zurück, das verwendet werden kann, um über alle Elemente in der Sammlung zu iterieren. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Gibt eine Schriftart mit dem angegebenen Namen zurück. |
| [idx_get](./idx_get/)(int32_t) | Gibt eine Schriftart am angegebenen Index zurück. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_EmbedSystemFonts](./set_embedsystemfonts/)(bool) | Setter für [Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts](./get_embedsystemfonts/). |
| [set_EmbedTrueTypeFonts](./set_embedtruetypefonts/)(bool) | Setter für [Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts](./get_embedtruetypefonts/). |
| [set_SaveSubsetFonts](./set_savesubsetfonts/)(bool) | Setter für [Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts](./get_savesubsetfonts/). |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Beschreibung |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Hinweise


Elemente sind [FontInfo](../fontinfo/) Objekte.

Sie erstellen keine Instanzen dieser Klasse direkt. Verwenden Sie die [FontInfos](../../aspose.words/documentbase/get_fontinfos/) Eigenschaft, um auf die Sammlung von im Dokument definierten Schriftarten zuzugreifen.

## Beispiele



Zeigt, wie man die Details der im Dokument vorhandenen Schriften ausgibt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// Gibt alle verwendeten und nicht verwendeten Schriften im Dokument aus.
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```


Zeigt, wie ein Dokument mit eingebetteten TrueType‑Schriftarten gespeichert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> fontInfos = doc->get_FontInfos();
fontInfos->set_EmbedTrueTypeFonts(embedAllFonts);
fontInfos->set_EmbedSystemFonts(embedAllFonts);
fontInfos->set_SaveSubsetFonts(embedAllFonts);

doc->Save(get_ArtifactsDir() + u"Font.FontInfoCollection.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
