---
title: "Aspose::Words::Fonts::FontInfoCollection classe"
linktitle: "FontInfoCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::FontInfoCollection classe. Rappresenta una raccolta di caratteri usati in un documento. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.fonts/fontinfocollection/
---
## FontInfoCollection class


Rappresenta una collezione di caratteri utilizzati in un documento. Per saperne di più, visita l'articolo di documentazione [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontInfoCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fonts::FontInfo>>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Contains](./contains/)(const System::String\&) | Determina se la raccolta contiene un carattere con il nome specificato. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Ottiene il numero di elementi contenuti nella raccolta. |
| [get_EmbedSystemFonts](./get_embedsystemfonts/)() const | Specifica se incorporare o meno i caratteri di sistema nel documento. Il valore predefinito per questa proprietà è **false**. Questa opzione funziona solo quando l'opzione [EmbedTrueTypeFonts](./get_embedtruetypefonts/) è impostata su **true**. |
| [get_EmbedTrueTypeFonts](./get_embedtruetypefonts/)() const | Specifica se incorporare o meno i caratteri TrueType in un documento al momento del salvataggio. Il valore predefinito per questa proprietà è **false**. |
| [get_SaveSubsetFonts](./get_savesubsetfonts/)() const | Specifica se salvare o meno un sottoinsieme dei caratteri TrueType incorporati con il documento. Il valore predefinito per questa proprietà è **false**. Questa opzione funziona solo quando la proprietà [EmbedTrueTypeFonts](./get_embedtruetypefonts/) è impostata su **true**. |
| [GetEnumerator](./getenumerator/)() override | Restituisce un oggetto enumeratore che può essere usato per iterare su tutti gli elementi della raccolta. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Ottiene un carattere con il nome specificato. |
| [idx_get](./idx_get/)(int32_t) | Ottiene un carattere all'indice specificato. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_EmbedSystemFonts](./set_embedsystemfonts/)(bool) | Impostatore per [Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts](./get_embedsystemfonts/). |
| [set_EmbedTrueTypeFonts](./set_embedtruetypefonts/)(bool) | Impostatore per [Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts](./get_embedtruetypefonts/). |
| [set_SaveSubsetFonts](./set_savesubsetfonts/)(bool) | Impostatore per [Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts](./get_savesubsetfonts/). |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Descrizione |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Note


Gli elementi sono oggetti [FontInfo](../fontinfo/).

Non si creano istanze di questa classe direttamente. Usa la proprietà [FontInfos](../../aspose.words/documentbase/get_fontinfos/) per accedere alla raccolta di caratteri definiti nel documento.

## Esempi



Mostra come stampare i dettagli dei caratteri presenti in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// Stampa tutti i caratteri utilizzati e non utilizzati nel documento.
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```


Mostra come salvare un documento con caratteri TrueType incorporati.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> fontInfos = doc->get_FontInfos();
fontInfos->set_EmbedTrueTypeFonts(embedAllFonts);
fontInfos->set_EmbedSystemFonts(embedAllFonts);
fontInfos->set_SaveSubsetFonts(embedAllFonts);

doc->Save(get_ArtifactsDir() + u"Font.FontInfoCollection.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
