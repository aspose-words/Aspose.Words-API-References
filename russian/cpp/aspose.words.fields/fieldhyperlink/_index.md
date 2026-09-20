---
title: "Aspose::Words::Fields::FieldHyperlink class"
linktitle: "FieldHyperlink"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldHyperlink class. Реализует поле HYPERLINK. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 53000
url: /ru/cpp/aspose.words.fields/fieldhyperlink/
---
## FieldHyperlink class


Реализует поле HYPERLINK. Чтобы узнать больше, посетите статью документации [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) .

```cpp
class FieldHyperlink : public Aspose::Words::Fields::Field,
                       public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                       public Aspose::Words::Fields::IFieldResultFormatProvider
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Address](./get_address/)() | Получает или задает расположение, куда переходит эта гиперссылка. |
| [get_DisplayResult](../field/get_displayresult/)() | Получает текст, представляющий отображаемый результат поля. |
| [get_End](../field/get_end/)() const | Получает узел, представляющий конец поля. |
| [get_FieldEnd](../field/get_fieldend/)() const | Получает узел, представляющий конец поля. |
| [get_FieldStart](../field/get_fieldstart/)() const | Получает узел, представляющий начало поля. |
| [get_Format](../field/get_format/)() | Получает объект [FieldFormat](../fieldformat/), который предоставляет типизированный доступ к форматированию поля. |
| [get_IsDirty](../field/get_isdirty/)() | Получает или задает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |
| [get_IsImageMap](./get_isimagemap/)() | Получает или задает, следует ли добавлять координаты к гиперссылке для серверной карты изображений. |
| [get_IsLocked](../field/get_islocked/)() | Получает или задает, заблокировано ли поле (не должно пересчитывать свой результат). |
| [get_LocaleId](../field/get_localeid/)() | Получает или задает LCID поля. |
| [get_OpenInNewWindow](./get_openinnewwindow/)() | Получает или задает, открывать ли целевой сайт в новом окне веб-браузера. |
| [get_Result](../field/get_result/)() | Получает или задает текст, находящийся между разделителем поля и его концом. |
| [get_ScreenTip](./get_screentip/)() | Получает или задает текст подсказки ScreenTip для гиперссылки. |
| [get_Separator](../field/get_separator/)() | Получает узел, представляющий разделитель поля. Может быть **null**. |
| [get_Start](../field/get_start/)() const | Получает узел, представляющий начало поля. |
| [get_SubAddress](./get_subaddress/)() | Получает или задает расположение в файле, например закладку, куда переходит эта гиперссылка. |
| [get_Target](./get_target/)() | Получает или задает цель, на которую должна перенаправляться ссылка. |
| virtual [get_Type](../field/get_type/)() const | Получает тип поля Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). Включены как код поля, так и результат дочерних полей. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла, возвращает родительский абзац. Если поле уже удалено, возвращает **null**. |
| [set_Address](./set_address/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldHyperlink::get_Address](./get_address/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsImageMap](./set_isimagemap/)(bool) | Сеттер для [Aspose::Words::Fields::FieldHyperlink::get_IsImageMap](./get_isimagemap/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Сеттер для [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_OpenInNewWindow](./set_openinnewwindow/)(bool) | Сеттер для [Aspose::Words::Fields::FieldHyperlink::get_OpenInNewWindow](./get_openinnewwindow/). |
| [set_Result](../field/set_result/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_ScreenTip](./set_screentip/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldHyperlink::get_ScreenTip](./get_screentip/). |
| [set_SubAddress](./set_subaddress/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldHyperlink::get_SubAddress](./get_subaddress/). |
| [set_Target](./set_target/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldHyperlink::get_Target](./get_target/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Выполняет отсоединение поля. |
| [Update](../field/update/)() | Выполняет обновление поля. Вызывает исключение, если поле уже обновляется. |
| [Update](../field/update/)(bool) | Выполняет обновление поля. Выбрасывает исключение, если поле уже обновляется. |

## Примеры



Показывает, как использовать поля HYPERLINK для ссылки на документы в локальной файловой системе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldHyperlink, true));

// Когда мы щёлкаем это поле HYPERLINK в Microsoft Word,
// оно откроет связанный документ, а затем разместит курсор в указанной закладке.
field->set_Address(get_MyDir() + u"Bookmarks.docx");
field->set_SubAddress(u"MyBookmark3");
field->set_ScreenTip(System::String(u"Open ") + field->get_Address() + u" on bookmark " + field->get_SubAddress() + u" in a new window");

builder->Writeln();

// Когда мы щёлкаем это поле HYPERLINK в Microsoft Word,
// оно откроет связанный документ и автоматически прокрутит вниз до указанного iframe.
field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldHyperlink, true));
field->set_Address(get_MyDir() + u"Iframes.html");
field->set_ScreenTip(System::String(u"Open ") + field->get_Address());
field->set_Target(u"iframe_3");
field->set_OpenInNewWindow(true);
field->set_IsImageMap(false);

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.HYPERLINK.docx");
```

## См. также

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
