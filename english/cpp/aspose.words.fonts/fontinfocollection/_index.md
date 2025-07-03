---
title: Aspose::Words::Fonts::FontInfoCollection class
linktitle: FontInfoCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontInfoCollection class. Represents a collection of fonts used in a document. To learn more, visit the  documentation article in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.fonts/fontinfocollection/
---
## FontInfoCollection class


Represents a collection of fonts used in a document. To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) documentation article.

```cpp
class FontInfoCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fonts::FontInfo>>
```

## Methods

| Method | Description |
| --- | --- |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Contains](./contains/)(const System::String\&) | Determines whether the collection contains a font with the given name. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Gets the number of elements contained in the collection. |
| [get_EmbedSystemFonts](./get_embedsystemfonts/)() const | Specifies whether or not to embed System fonts into the document. Default value for this property is **false**. This option works only when [EmbedTrueTypeFonts](./get_embedtruetypefonts/) option is set to **true**. |
| [get_EmbedTrueTypeFonts](./get_embedtruetypefonts/)() const | Specifies whether or not to embed TrueType fonts in a document when it is saved. Default value for this property is **false**. |
| [get_SaveSubsetFonts](./get_savesubsetfonts/)() const | Specifies whether or not to save a subset of the embedded TrueType fonts with the document. Default value for this property is **false**. This option works only when [EmbedTrueTypeFonts](./get_embedtruetypefonts/) property is set to **true**. |
| [GetEnumerator](./getenumerator/)() override | Returns an enumerator object that can be used to iterate over all items in the collection. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Gets a font with the specified name. |
| [idx_get](./idx_get/)(int32_t) | Gets a font at the specified index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_EmbedSystemFonts](./set_embedsystemfonts/)(bool) | Setter for [Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts](./get_embedsystemfonts/). |
| [set_EmbedTrueTypeFonts](./set_embedtruetypefonts/)(bool) | Setter for [Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts](./get_embedtruetypefonts/). |
| [set_SaveSubsetFonts](./set_savesubsetfonts/)(bool) | Setter for [Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts](./get_savesubsetfonts/). |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Description |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Remarks


Items are [FontInfo](../fontinfo/) objects.

You do not create instances of this class directly. Use the [FontInfos](../../aspose.words/documentbase/get_fontinfos/) property to access the collection of fonts defined in the document.

## Examples



Shows how to print the details of what fonts are present in a document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// Print all the used and unused fonts in the document.
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```


Shows how to save a document with embedded TrueType fonts. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> fontInfos = doc->get_FontInfos();
fontInfos->set_EmbedTrueTypeFonts(embedAllFonts);
fontInfos->set_EmbedSystemFonts(embedAllFonts);
fontInfos->set_SaveSubsetFonts(embedAllFonts);

doc->Save(get_ArtifactsDir() + u"Font.FontInfoCollection.docx");
```

## See Also

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
