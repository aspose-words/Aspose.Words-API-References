---
title: "Aspose::Words::MailMerging::MailMerge::Execute метод"
linktitle: "Выполнить"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::MailMerging::MailMerge::Execute метод. Выполняет операцию слияния почты для одной записи в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.mailmerging/mailmerge/execute/
---
## MailMerge::Execute(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\&) method


Выполняет операцию слияния почты для одной записи.

```cpp
void Aspose::Words::MailMerging::MailMerge::Execute(const System::ArrayPtr<System::String> &fieldNames, const System::ArrayPtr<System::SharedPtr<System::Object>> &values)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldNames | const System::ArrayPtr\<System::String\>\& | Массив имен полей слияния. Имена полей не чувствительны к регистру. Если встречается имя поля, которое не найдено в документе, оно игнорируется. |
| values | const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\& | Массив значений, которые будут вставлены в поля слияния. Количество элементов в этом массиве должно совпадать с количеством элементов в *fieldNames*. |
## Примечания


Используйте этот метод, чтобы заполнить поля слияния почты в документе значениями из массива объектов.

Этот метод объединяет данные только для одной записи. Массив имен полей и массив значений представляют данные одной записи.

Этот метод не использует регионы слияния почты.

Этот метод игнорирует параметр [RemoveUnusedRegions](../../mailmergecleanupoptions/).

## Примеры



Показывает, как объединить изображение из URI в качестве данных слияния почты в MERGEFIELD.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// MERGEFIELDs с тегами \"Image:\" получат изображение во время слияния почты.
// Строка после двоеточия в теге \"Image:\" соответствует имени столбца
// в источнике данных, ячейки которого содержат URI файлов изображений.
builder->InsertField(u"MERGEFIELD  Image:logo_FromWeb ");
builder->InsertField(u"MERGEFIELD  Image:logo_FromFileSystem ");

// Создайте источник данных, содержащий URI изображений, которые мы будем объединять.
// URI может быть веб‑URL, указывающим на изображение, или именем файла изображения в локальной файловой системе.
System::ArrayPtr<System::String> columns = System::MakeArray<System::String>({u"logo_FromWeb", u"logo_FromFileSystem"});
System::ArrayPtr<System::SharedPtr<System::Object>> URIs = System::MakeArray<System::SharedPtr<System::Object>>({System::ExplicitCast<System::Object>(get_ImageUrl()), System::ExplicitCast<System::Object>(get_ImageDir() + u"Logo.jpg")});

// Выполните слияние почты на источнике данных с одной строкой.
doc->get_MailMerge()->Execute(columns, URIs);

doc->Save(get_ArtifactsDir() + u"MailMergeEvent.ImageFromUrl.docx");
```

## См. также

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::Execute(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) method


Выполняет слияние почты из пользовательского источника данных.

```cpp
void Aspose::Words::MailMerging::MailMerge::Execute(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> &dataSource)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| dataSource | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\& | Объект, реализующий пользовательский интерфейс источника данных для слияния почты. |
## Примечания


Используйте этот метод для заполнения полей слияния почты в документе значениями из любого источника данных, например списка, хеш-таблицы или объектов. Вам необходимо написать собственный класс, реализующий интерфейс [IMailMergeDataSource](../../imailmergedatasource/).

Вы можете использовать этот метод только когда [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) имеет значение **false**, то есть вам не требуется поддержка языков с письмом справа налево (например, арабского или иврита).

Этот метод игнорирует параметр [RemoveUnusedRegions](../../mailmergecleanupoptions/).

## См. также

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
