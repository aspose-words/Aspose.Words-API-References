---
title: "Метод Aspose::Words::Range::UpdateFields"
linktitle: "UpdateFields"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Range::UpdateFields. Обновляет значения полей документа в этом диапазоне в C++."
type: docs
weight: 15000
url: /ru/cpp/aspose.words/range/updatefields/
---
## Range::UpdateFields method


Обновляет значения полей документа в этом диапазоне.

```cpp
void Aspose::Words::Range::UpdateFields()
```

## Примечания


Когда вы открываете, изменяете и затем сохраняете документ, Aspose.Words не обновляет поля автоматически, а оставляет их неизменными. Поэтому обычно следует вызвать этот метод перед сохранением, если вы программно изменили документ и хотите убедиться, что правильные (вычисленные) значения полей отображаются в сохранённом документе.

Нет необходимости обновлять поля после выполнения слияния почты, поскольку слияние почты является видом обновления полей и автоматически обновляет все поля в документе.

Этот метод не обновляет все типы полей. Для подробного списка поддерживаемых типов полей см. Руководство программиста.

Этот метод не обновляет поля, связанные с алгоритмами разметки страниц (например, PAGE, PAGES, PAGEREF). Поля, связанные с разметкой страниц, обновляются при рендеринге документа или вызове [UpdatePageLayout](../../document/updatepagelayout/).

Чтобы обновить поля во всём документе, используйте [UpdateFields](../../document/updatefields/).

## Примеры



Показывает, как обновить все поля в диапазоне.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertField(u" DOCPROPERTY Category");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);
builder->InsertField(u" DOCPROPERTY Category");

// Вышеуказанные поля DOCPROPERTY отобразят значение этого встроенного свойства документа.
doc->get_BuiltInDocumentProperties()->set_Category(u"MyCategory");

// Если мы обновим значение свойства документа, нам потребуется обновить все поля DOCPROPERTY, чтобы они отобразили его.
ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// Обновите все поля, которые находятся в диапазоне первого раздела.
doc->get_FirstSection()->get_Range()->UpdateFields();

ASSERT_EQ(u"MyCategory", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
```

## См. также

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
