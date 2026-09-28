---
title: "Aspose::Words::Hyphenation::IsDictionaryRegistered method"
linktitle: "IsDictionaryRegistered"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Hyphenation::IsDictionaryRegistered. Возвращает false, если для указанного языка нет зарегистрированного словаря или если зарегистрирован Null‑словарь, иначе возвращает true в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words/hyphenation/isdictionaryregistered/
---
## Hyphenation::IsDictionaryRegistered method


Возвращает **false**, если для указанного языка не зарегистрирован словарь или зарегистрирован Null‑словарь, **true** в противном случае.

```cpp
static bool Aspose::Words::Hyphenation::IsDictionaryRegistered(const System::String &language)
```


## Примеры



Показывает, как зарегистрировать словарь переносов.
```cpp
// Словарь переносов содержит список строк, определяющих правила переноса для языка словаря.
// Когда документ содержит строки текста, в которых слово может быть разбито и продолжено на следующей строке,
// перенос будет просматривать список строк словаря в поиске подстрок этого слова.
// Если словарь содержит подстроку, то перенос разделит слово на две строки
// по этой подстроке и добавит дефис к первой части.
// Зарегистрируйте файл словаря из локальной файловой системы для локали "de-CH".
Aspose::Words::Hyphenation::RegisterDictionary(u"de-CH", get_MyDir() + u"hyph_de_CH.dic");

ASSERT_TRUE(Aspose::Words::Hyphenation::IsDictionaryRegistered(u"de-CH"));

// Откройте документ, содержащий текст с локалью, соответствующей нашей локали словаря,
// и сохраните его в формат фиксированных страниц. Текст в этом документе будет перенесён.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"German text.docx");

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->LINQ_OfType<System::SharedPtr<Aspose::Words::Run> >()->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::Run>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Run> r)>>([](System::SharedPtr<Aspose::Words::Run> r) -> bool
{
    return r->get_Font()->get_LocaleId() == System::MakeObject<System::Globalization::CultureInfo>(u"de-CH")->get_LCID();
}))));

doc->Save(get_ArtifactsDir() + u"Hyphenation.Dictionary.Registered.pdf");

// Перезагрузите документ после отмены регистрации словаря,
// и сохраните его в другой PDF, в котором текст не будет перенесён.
Aspose::Words::Hyphenation::UnregisterDictionary(u"de-CH");

ASSERT_FALSE(Aspose::Words::Hyphenation::IsDictionaryRegistered(u"de-CH"));

doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"German text.docx");
doc->Save(get_ArtifactsDir() + u"Hyphenation.Dictionary.Unregistered.pdf");
```

## См. также

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
