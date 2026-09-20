---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_FullDate метод"
linktitle: "get_FullDate"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_FullDate метод. Указывает полную дату и время последнего ввода в этот SDT в C++."
type: docs
weight: 16000
url: /ru/cpp/aspose.words.markup/structureddocumenttag/get_fulldate/
---
## StructuredDocumentTag::get_FullDate method


Указывает полную дату и время, последним введённые в этот **SDT**.

```cpp
System::DateTime Aspose::Words::Markup::StructuredDocumentTag::get_FullDate()
```

## Примечания


Доступ к этому свойству будет работать только для типа SDT [Date](../../sdttype/).

Для всех остальных типов SDT будет возникать исключение.

## Примеры



Показывает, как запросить у пользователя ввод даты с помощью структурированного тега документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Вставьте структурированный тег документа, который запрашивает у пользователя ввод даты.
// В Microsoft Word этот элемент известен как "Date picker content control".
// Когда мы щёлкаем по стрелке в правом конце этого тега в Microsoft Word,
// Мы увидим всплывающее окно в виде кликабельного календаря.
// Мы можем использовать это всплывающее окно, чтобы выбрать дату, которую будет отображать тег.
auto sdtDate = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Date, Aspose::Words::Markup::MarkupLevel::Inline);

// Отобразите дату в соответствии с саудовским арабским локалем.
sdtDate->set_DateDisplayLocale(System::Globalization::CultureInfo::GetCultureInfo(u"ar-SA")->get_LCID());

// Установите формат, в котором будет отображаться дата.
sdtDate->set_DateDisplayFormat(u"dd MMMM, yyyy");
sdtDate->set_DateStorageFormat(Aspose::Words::Markup::SdtDateStorageFormat::DateTime);

// Отобразите дату в соответствии с хиджраским календарём.
sdtDate->set_CalendarType(Aspose::Words::Markup::SdtCalendarType::Hijri);

// Прежде чем пользователь выберет дату в Microsoft Word, тег отобразит текст "Нажмите здесь, чтобы ввести дату.".
// В соответствии с календарём тега установите свойство "FullDate", чтобы тег отобразил дату по умолчанию.
sdtDate->set_FullDate(System::DateTime(1440, 10, 20));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(sdtDate);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Date.docx");
```

## См. также

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
