---
title: "Aspose::Words::Range::Replace метод"
linktitle: "Replace"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Range::Replace метод. Заменяет все вхождения символьного шаблона, указанного регулярным выражением, другой строкой в C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words/range/replace/
---
## Range::Replace(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Заменяет все вхождения шаблона символов, указанного регулярным выражением, другой строкой.

```cpp
int32_t Aspose::Words::Range::Replace(const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| шаблон | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Шаблон регулярного выражения, используемый для поиска совпадений. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |

### ReturnValue

Количество выполненных замен.
## Примечания


Заменяет полное совпадение, захваченное регулярным выражением.

Метод способен обрабатывать разрывы как в строках шаблона, так и в строках замены.

Вам следует использовать специальные мета-символы, если необходимо работать с разрывами:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break



## Примеры



Показывает, как заменить все вхождения шаблона регулярного выражения другим текстом.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"I decided to get the curtains in gray, ideal for the grey-accented room.");

doc->get_Range()->Replace(System::MakeObject<System::Text::RegularExpressions::Regex>(u"gr(a|e)y"), u"lavender");

ASSERT_EQ(u"I decided to get the curtains in lavender, ideal for the lavender-accented room.", doc->GetText().Trim());
```

## См. также

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Range::Replace(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Заменяет все вхождения шаблона символов, указанного регулярным выражением, другой строкой.

```cpp
int32_t Aspose::Words::Range::Replace(const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| шаблон | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Шаблон регулярного выражения, используемый для поиска совпадений. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) объект для указания дополнительных параметров. |

### ReturnValue

Количество выполненных замен.
## Примечания


Заменяет полное совпадение, захваченное регулярным выражением.

Метод способен обрабатывать разрывы как в строках шаблона, так и в строках замены.

Вам следует использовать специальные мета-символы, если необходимо работать с разрывами:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break
* **%&&** - & character



## См. также

* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Range::Replace(const System::String\&, const System::String\&) method


Заменяет все вхождения указанного шаблона строкового символа на строку‑заменитель.

```cpp
int32_t Aspose::Words::Range::Replace(const System::String &pattern, const System::String &replacement)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| шаблон | const System::String\& | Строка, которую нужно заменить. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |

### ReturnValue

Количество выполненных замен.
## Примечания


Шаблон не будет использоваться как регулярное выражение. Пожалуйста, используйте [Replace()](../), если вам нужны регулярные выражения.

Использовано сравнение без учёта регистра.

Метод способен обрабатывать разрывы как в строках шаблона, так и в строках замены.

Вам следует использовать специальные мета-символы, если необходимо работать с разрывами:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break



## Примеры



Показывает, как выполнить операцию поиска и замены текста в содержимом документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Greetings, _FullName_!");

// Выполните операцию поиска и замены в содержимом нашего документа и проверьте количество выполненных замен.
int32_t replacementCount = doc->get_Range()->Replace(u"_FullName_", u"John Doe");

ASSERT_EQ(1, replacementCount);
ASSERT_EQ(u"Greetings, John Doe!", doc->GetText().Trim());
```


Показывает, как добавить форматирование к абзацам, в которых операция поиска и замены нашла совпадения.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Every paragraph that ends with a full stop like this one will be right aligned.");
builder->Writeln(u"This one will not!");
builder->Write(u"This one also will.");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());

// Мы можем использовать объект "FindReplaceOptions" для изменения процесса поиска и замены.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Установите свойство "Alignment" в значение "ParagraphAlignment.Right", чтобы выровнять каждый абзац по правому краю.
// которые содержат совпадение, найденное операцией поиска и замены.
options->get_ApplyParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);

// Замените каждую точку, стоящую непосредственно перед разрывом абзаца, на восклицательный знак.
int32_t count = doc->get_Range()->Replace(u".&p", u"!&p", options);

ASSERT_EQ(2, count);
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(System::String(u"Every paragraph that ends with a full stop like this one will be right aligned!\r") + u"This one will not!\r" + u"This one also will!", doc->GetText().Trim());
```

## См. также

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Range::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Заменяет все вхождения указанного шаблона строкового символа на строку‑заменитель.

```cpp
int32_t Aspose::Words::Range::Replace(const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| шаблон | const System::String\& | Строка, которую нужно заменить. |
| замена | const System::String\& | Строка для замены всех вхождений шаблона. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) объект для указания дополнительных параметров. |

### ReturnValue

Количество выполненных замен.
## Примечания


Шаблон не будет использоваться как регулярное выражение. Пожалуйста, используйте [Replace()](../), если вам нужны регулярные выражения.

Метод способен обрабатывать разрывы как в строках шаблона, так и в строках замены.

Вам следует использовать специальные мета-символы, если необходимо работать с разрывами:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break
* **%&&** - & character



## Примеры



Показывает, как заменить текст в нижнем колонтитуле документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footer.docx");

System::SharedPtr<Aspose::Words::HeaderFooterCollection> headersFooters = doc->get_FirstSection()->get_HeadersFooters();
System::SharedPtr<Aspose::Words::HeaderFooter> footer = headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_MatchCase(false);
options->set_FindWholeWordsOnly(false);

int32_t currentYear = System::DateTime::get_Now().get_Year();
footer->get_Range()->Replace(u"(C) 2006 Aspose Pty Ltd.", System::String::Format(u"Copyright (C) {0} by Aspose Pty Ltd.", currentYear), options);

doc->Save(get_ArtifactsDir() + u"HeaderFooter.ReplaceText.docx");
```


Показывает, как переключать чувствительность к регистру при выполнении операции поиска и замены.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Ruby bought a ruby necklace.");

// Мы можем использовать объект "FindReplaceOptions" для изменения процесса поиска и замены.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Установите флаг "MatchCase" в значение "true", чтобы применять чувствительность к регистру при поиске строк для замены.
// Установите флаг "MatchCase" в значение "false", чтобы игнорировать регистр символов при поиске текста для замены.
options->set_MatchCase(matchCase);

doc->get_Range()->Replace(u"Ruby", u"Jade", options);

ASSERT_EQ(matchCase ? System::String(u"Jade bought a ruby necklace.") : System::String(u"Jade bought a Jade necklace."), doc->GetText().Trim());
```


Показывает, как переключать операции поиска и замены только отдельными словами.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jackson will meet you in Jacksonville.");

// Мы можем использовать объект "FindReplaceOptions" для изменения процесса поиска и замены.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Установите флаг "FindWholeWordsOnly" в значение "true", чтобы заменять найденный текст, если он не является частью другого слова.
// Установите флаг "FindWholeWordsOnly" в значение "false", чтобы заменять весь текст независимо от его окружения.
options->set_FindWholeWordsOnly(findWholeWordsOnly);

doc->get_Range()->Replace(u"Jackson", u"Louis", options);

ASSERT_EQ(findWholeWordsOnly ? System::String(u"Louis will meet you in Jacksonville.") : System::String(u"Louis will meet you in Louisville."), doc->GetText().Trim());
```


Показывает, как заменить все вхождения строки текста в таблице и ячейке.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Carrots");
builder->InsertCell();
builder->Write(u"50");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Potatoes");
builder->InsertCell();
builder->Write(u"50");
builder->EndTable();

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_MatchCase(true);
options->set_FindWholeWordsOnly(true);

// Выполните операцию поиска и замены во всей таблице.
table->get_Range()->Replace(u"Carrots", u"Eggs", options);

// Выполните операцию поиска и замены в последней ячейке последней строки таблицы.
table->get_LastRow()->get_LastCell()->get_Range()->Replace(u"50", u"20", options);

ASSERT_EQ(System::String(u"Eggs\a50\a\a") + u"Potatoes\a20\a\a", table->GetText().Trim());
```

## См. также

* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
