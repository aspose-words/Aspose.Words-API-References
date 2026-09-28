---
title: "класс Aspose::Words::Fonts::FontInfoCollection"
linktitle: "FontInfoCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "класс Aspose::Words::Fonts::FontInfoCollection. Представляет коллекцию шрифтов, используемых в документе. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.fonts/fontinfocollection/
---
## FontInfoCollection class


Представляет коллекцию шрифтов, используемых в документе. Чтобы узнать больше, посетите статью документации [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontInfoCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fonts::FontInfo>>
```

## Методы

| Метод | Описание |
| --- | --- |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Contains](./contains/)(const System::String\&) | Определяет, содержит ли коллекция шрифт с указанным именем. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Получает количество элементов, содержащихся в коллекции. |
| [get_EmbedSystemFonts](./get_embedsystemfonts/)() const | Указывает, следует ли встраивать системные шрифты в документ. Значение по умолчанию для этого свойства — **false**. Эта опция работает только когда параметр [EmbedTrueTypeFonts](./get_embedtruetypefonts/) установлен в **true**. |
| [get_EmbedTrueTypeFonts](./get_embedtruetypefonts/)() const | Указывает, следует ли встраивать TrueType шрифты в документ при сохранении. Значение по умолчанию для этого свойства — **false**. |
| [get_SaveSubsetFonts](./get_savesubsetfonts/)() const | Указывает, следует ли сохранять подмножество встроенных TrueType шрифтов в документе. Значение по умолчанию для этого свойства — **false**. Эта опция работает только когда свойство [EmbedTrueTypeFonts](./get_embedtruetypefonts/) установлено в **true**. |
| [GetEnumerator](./getenumerator/)() override | Возвращает объект‑перечислитель, который можно использовать для перебора всех элементов в коллекции. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Получает шрифт с указанным именем. |
| [idx_get](./idx_get/)(int32_t) | Получает шрифт по указанному индексу. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_EmbedSystemFonts](./set_embedsystemfonts/)(bool) | Сеттер для [Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts](./get_embedsystemfonts/). |
| [set_EmbedTrueTypeFonts](./set_embedtruetypefonts/)(bool) | Сеттер для [Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts](./get_embedtruetypefonts/). |
| [set_SaveSubsetFonts](./set_savesubsetfonts/)(bool) | Сеттер для [Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts](./get_savesubsetfonts/). |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Типовое определение | Описание |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Примечания


Элементы являются объектами [FontInfo](../fontinfo/).

Вы не создаёте экземпляры этого класса напрямую. Используйте свойство [FontInfos](../../aspose.words/documentbase/get_fontinfos/), чтобы получить доступ к коллекции шрифтов, определённых в документе.

## Примеры



Показывает, как вывести детали о шрифтах, присутствующих в документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// Вывести все используемые и неиспользуемые шрифты в документе.
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```


Показывает, как сохранить документ со встроенными TrueType шрифтами.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> fontInfos = doc->get_FontInfos();
fontInfos->set_EmbedTrueTypeFonts(embedAllFonts);
fontInfos->set_EmbedSystemFonts(embedAllFonts);
fontInfos->set_SaveSubsetFonts(embedAllFonts);

doc->Save(get_ArtifactsDir() + u"Font.FontInfoCollection.docx");
```

## См. также

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
