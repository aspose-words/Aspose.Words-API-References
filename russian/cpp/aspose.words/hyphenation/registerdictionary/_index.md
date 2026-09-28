---
title: "Aspose::Words::Hyphenation::RegisterDictionary метод"
linktitle: "RegisterDictionary"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Hyphenation::RegisterDictionary метод. Регистрирует и загружает словарь переноса для указанного языка из потока. Выбрасывает исключение, если словарь не может быть прочитан или имеет неверный формат в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words/hyphenation/registerdictionary/
---
## Hyphenation::RegisterDictionary(const System::String\&, const System::SharedPtr\<System::IO::Stream\>\&) method


Регистрирует и загружает словарь переносов для указанного языка из потока. Выбрасывает исключение, если словарь нельзя прочитать или он имеет неверный формат.

```cpp
static void Aspose::Words::Hyphenation::RegisterDictionary(const System::String &language, const System::SharedPtr<System::IO::Stream> &stream)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| language | const System::String\& | Имя языка, например "en-US". См. документацию .NET по "culture name" и RFC 4646 для получения подробностей. |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | Поток для файла словаря в формате OpenOffice. |

## См. также

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Hyphenation::RegisterDictionary(const System::String\&, const System::String\&) method


Регистрирует и загружает словарь переноса для указанного языка из файла. Выбрасывает исключение, если словарь не может быть прочитан или имеет неверный формат. Этот метод также может использоваться для регистрации Null‑словаря, чтобы предотвратить вызов [Callback](../get_callback/) неоднократно для одного и того же языка.

```cpp
static void Aspose::Words::Hyphenation::RegisterDictionary(const System::String &language, const System::String &fileName)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| language | const System::String\& | Имя языка, например "en-US". См. документацию .NET по "culture name" и RFC 4646 для получения подробностей. |
| fileName | const System::String\& | Путь к файлу словаря в формате Open Office. Если этот параметр имеет значение **null** или пустую строку, то регистрируется Null‑словарь, и обратный вызов больше не будет вызываться для этого языка. Чтобы снова включить обратный вызов, используйте метод [UnregisterDictionary()](../). |

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
## Hyphenation::RegisterDictionary(System::String, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static void Aspose::Words::Hyphenation::RegisterDictionary(System::String language, std::basic_istream<CharType, Traits> &stream)
```

## См. также

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
