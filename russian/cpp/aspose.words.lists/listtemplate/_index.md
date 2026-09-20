---
title: "Перечисление Aspose::Words::Lists::ListTemplate"
linktitle: "ListTemplate"
second_title: "Справочник API Aspose.Words для C++"
description: "Перечисление Aspose::Words::Lists::ListTemplate. Указывает один из предопределённых форматов списков, доступных в Microsoft Word на C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words.lists/listtemplate/
---
## ListTemplate enum


Указывает один из предопределённых форматов списка, доступных в Microsoft Word.

```cpp
enum class ListTemplate
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| BulletDefault | 0 | Список с маркерами по умолчанию, содержащий 9 уровней. Маркер первого уровня — диск, маркер второго уровня — круг, маркер третьего уровня — квадрат. Затем форматирование повторяется для остальных уровней. Каждый уровень отступает вправо на 0.25" относительно предыдущего уровня. Соответствует первому шаблону маркированного списка в диалоговом окне Маркеры и нумерация в Microsoft Word. |
| BulletDisk | n/a | То же, что и [BulletDefault](./). Соответствует первому шаблону маркированного списка в диалоговом окне Маркеры и нумерация в Microsoft Word. |
| BulletCircle | n/a | Маркер первого уровня — круг. Остальные уровни такие же, как в [BulletDefault](./). Соответствует второму шаблону маркированного списка в диалоговом окне Маркеры и нумерация в Microsoft Word. |
| BulletSquare | n/a | Маркер первого уровня — квадрат. Остальные уровни такие же, как в [BulletDefault](./). Соответствует третьему шаблону маркированного списка в диалоговом окне Маркеры и нумерация в Microsoft Word. |
| BulletDiamonds | n/a | Маркер первого уровня — символ Wingding «4-ромб». Остальные уровни такие же, как в [BulletDefault](./). Соответствует пятому шаблону маркированного списка в диалоговом окне Маркеры и нумерация в Microsoft Word. |
| BulletArrowHead | n/a | Маркер первого уровня — символ Wingding «стрелка». Остальные уровни такие же, как в [BulletDefault](./). Соответствует шестому шаблону маркированного списка в диалоговом окне Маркеры и нумерация в Microsoft Word. |
| BulletTick | n/a | Маркер первого уровня — символ Wingding «галочка». Остальные уровни такие же, как в [BulletDefault](./). Соответствует седьмому шаблону маркированного списка в диалоговом окне Маркеры и нумерация в Microsoft Word. |
| NumberDefault | н/д | Нумерованный список по умолчанию, содержащий 9 уровней. Арабская нумерация (1., 2., 3., ...) для первого уровня, нумерация строчными буквами (a., b., c., ...) для второго уровня, строчная римская нумерация (i., ii., iii., ...) для третьего уровня. Затем форматирование повторяется для остальных уровней. Каждый уровень отступает вправо на 0.25" относительно предыдущего уровня. Соответствует первому шаблону нумерованного списка в диалоговом окне Маркеры и нумерация в Microsoft Word. |
| NumberArabicDot | n/a | То же, что и [NumberDefault](./). Соответствует первому шаблону нумерованного списка в диалоговом окне Маркеры и нумерация в Microsoft Word. |
| NumberArabicParenthesis | n/a | Номер первого уровня — "1)". Остальные уровни такие же, как в [NumberDefault](./). Соответствует второму шаблону нумерованного списка в диалоговом окне Маркеры и нумерация в Microsoft Word. |
| NumberUppercaseRomanDot | n/a | Номер первого уровня — "I.". Остальные уровни такие же, как в [NumberDefault](./). Соответствует третьему шаблону нумерованного списка в диалоговом окне Маркеры и нумерация в Microsoft Word. |
| NumberUppercaseLetterDot | n/a | Номер первого уровня — "A.". Остальные уровни такие же, как в [NumberDefault](./). Соответствует четвертому шаблону нумерованного списка в диалоговом окне Маркеры и нумерация в Microsoft Word. |
| NumberLowercaseLetterParenthesis | n/a | Номер первого уровня — "a)". Остальные уровни такие же, как в [NumberDefault](./). Соответствует пятому шаблону нумерованного списка в диалоговом окне Маркеры и нумерация в Microsoft Word. |
| NumberLowercaseLetterDot | n/a | Номер первого уровня — "a.". Остальные уровни такие же, как в [NumberDefault](./). Соответствует 6‑му шаблону нумерованного списка в диалоговом окне Маркеры и нумерация в Microsoft Word. |
| NumberLowercaseRomanDot | n/a | Номер первого уровня — "i.". Остальные уровни такие же, как в [NumberDefault](./). Соответствует 7‑му шаблону нумерованного списка в диалоговом окне Маркеры и нумерация в Microsoft Word. |
| OutlineNumbers | н/д | Список с оглавлением, уровни которого нумеруются "1), a), i), (1), (a), (i), 1., a., i.". Соответствует 1‑му шаблону списка с оглавлением в диалоговом окне Маркеры и нумерация в Microsoft Word. |
| OutlineLegal | н/д | Список с оглавлением, уровни которого нумеруются "1., 1.1., 1.1.1, ...". Соответствует 2‑му шаблону списка с оглавлением в диалоговом окне Маркеры и нумерация в Microsoft Word. |
| OutlineBullets | н/д | Списки с оглавлением с различными маркерами для разных уровней. Соответствует 3‑му шаблону списка с оглавлением в диалоговом окне Маркеры и нумерация в Microsoft Word. |
| OutlineHeadingsArticleSection | н/д | Список с оглавлением, уровни которого связаны со стилями заголовков. Соответствует 4‑му шаблону списка с оглавлением в диалоговом окне Маркеры и нумерация в Microsoft Word. |
| OutlineHeadingsLegal | н/д | Список с оглавлением, уровни которого связаны со стилями заголовков. Соответствует 5‑му шаблону списка с оглавлением в диалоговом окне Маркеры и нумерация в Microsoft Word. |
| OutlineHeadingsNumbers | н/д | Список с оглавлением, уровни которого связаны со стилями заголовков. Соответствует 6‑му шаблону списка с оглавлением в диалоговом окне Маркеры и нумерация в Microsoft Word. |
| OutlineHeadingsChapter | н/д | Список с оглавлением, уровни которого связаны со стилями заголовков. Соответствует 7‑му шаблону списка с оглавлением в диалоговом окне Маркеры и нумерация в Microsoft Word. |

## Примечания


Значение шаблона списка используется в качестве параметра метода [Add()](../listcollection/add/).

Шаблоны списков Aspose.Words соответствуют 21 шаблону списков, доступным в диалоговом окне Маркеры и нумерация в Microsoft Word 2003.

## Примеры



Показывает, как работать с уровнями списка.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

// Список позволяет организовывать и оформлять наборы абзацев с помощью префиксных символов и отступов.
// Мы можем создавать вложенные списки, увеличивая уровень отступа.
// Мы можем начинать и завершать список, используя свойство "ListFormat" объекта document builder.
// Каждый абзац, который мы добавляем между началом и концом списка, становится элементом списка.
// Ниже представлены два типа списков, которые мы можем создать с помощью document builder.
// 1 -  Нумерованный список:
// Нумерованные списки создают логический порядок для своих абзацев, нумеруя каждый элемент.
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault));

ASSERT_TRUE(builder->get_ListFormat()->get_IsListItem());

// Установив свойство \"ListLevelNumber\", мы можем увеличить уровень списка
// чтобы начать автономный подсписок в текущем элементе списка.
// Шаблон списка Microsoft Word под названием \"NumberDefault\" использует цифры для создания уровней списка для первого уровня списка.
// Более глубокие уровни списка используют буквы и римские цифры в нижнем регистре.
for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// 2 -  Маркированный список:
// Этот список будет применять отступ и символ маркера (\"•\") перед каждым абзацем.
// Более глубокие уровни этого списка будут использовать разные символы, такие как \"■\" и \"○\".
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));

for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// Мы можем отключить форматирование списка, чтобы не форматировать последующие абзацы как списки, сняв флаг \"List\".
builder->get_ListFormat()->set_List(nullptr);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

doc->Save(get_ArtifactsDir() + u"Lists.SpecifyListLevel.docx");
```


Показывает, как перезапустить нумерацию в списке, скопировав список.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Список позволяет организовывать и оформлять наборы абзацев с помощью префиксных символов и отступов.
// Мы можем создавать вложенные списки, увеличивая уровень отступа.
// Мы можем начинать и завершать список, используя свойство "ListFormat" объекта document builder.
// Каждый абзац, который мы добавляем между началом и концом списка, становится элементом списка.
// Создайте список из шаблона Microsoft Word и настройте его первый уровень списка.
System::SharedPtr<Aspose::Words::Lists::List> list1 = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberArabicParenthesis);
list1->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Red());
list1->get_ListLevels()->idx_get(0)->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);

// Примените наш список к некоторым абзацам.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"List 1 starts below:");
builder->get_ListFormat()->set_List(list1);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

// Мы можем добавить копию существующего списка в коллекцию списков документа
// чтобы создать похожий список без изменения оригинала.
System::SharedPtr<Aspose::Words::Lists::List> list2 = doc->get_Lists()->AddCopy(list1);
list2->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Blue());
list2->get_ListLevels()->idx_get(0)->set_StartAt(10);

// Примените второй список к новым абзацам.
builder->Writeln(u"List 2 starts below:");
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.RestartNumberingUsingListCopy.docx");
```

## См. также

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
