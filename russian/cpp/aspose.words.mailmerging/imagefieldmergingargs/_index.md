---
title: "Aspose::Words::MailMerging::ImageFieldMergingArgs class"
linktitle: "ImageFieldMergingArgs"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::MailMerging::ImageFieldMergingArgs class. Предоставляет данные для события ImageFieldMerging(). Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.mailmerging/imagefieldmergingargs/
---
## ImageFieldMergingArgs class


Предоставляет данные для события [ImageFieldMerging()](../ifieldmergingcallback/imagefieldmerging/). Чтобы узнать больше, посетите статью документации [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class ImageFieldMergingArgs : public Aspose::Words::MailMerging::FieldMergingArgsBase
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Document](../fieldmergingargsbase/get_document/)() const | Возвращает объект [Document](../fieldmergingargsbase/get_document/), для которого выполняется слияние почты. |
| [get_DocumentFieldName](../fieldmergingargsbase/get_documentfieldname/)() const | Получает имя поля слияния, как указано в документе. |
| [get_Field](../fieldmergingargsbase/get_field/)() const | Получает объект, представляющий текущее поле слияния. |
| [get_FieldName](../fieldmergingargsbase/get_fieldname/)() const | Получает имя поля слияния в источнике данных. |
| [get_FieldValue](../fieldmergingargsbase/get_fieldvalue/)() const | Получает значение поля из источника данных. |
| [get_Image](./get_image/)() const | Указывает изображение, которое движок слияния почты должен вставить в документ. |
| [get_ImageFileName](./get_imagefilename/)() const | Устанавливает имя файла изображения, которое движок слияния почты должен вставить в документ. |
| [get_ImageHeight](./get_imageheight/)() const | Указывает высоту изображения для вставки в документ. |
| [get_ImageStream](./get_imagestream/)() const | Указывает поток, из которого движок слияния почты будет считывать изображение. |
| [get_ImageWidth](./get_imagewidth/)() const | Указывает ширину изображения для вставки в документ. |
| [get_RecordIndex](../fieldmergingargsbase/get_recordindex/)() const | Получает нулевой индекс записи, которая объединяется. |
| [get_Shape](./get_shape/)() const | Указывает форму, которую движок слияния почты должен вставить в документ. |
| [get_TableName](../fieldmergingargsbase/get_tablename/)() const | Получает имя таблицы данных для текущей операции слияния или пустую строку, если имя недоступно. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FieldValue](../fieldmergingargsbase/set_fieldvalue/)(const System::SharedPtr\<System::Object\>\&) | Устанавливает значение поля из источника данных. |
| [set_Image](./set_image/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Указывает изображение, которое движок слияния почты должен вставить в документ. |
| [set_ImageFileName](./set_imagefilename/)(const System::String\&) | Устанавливает имя файла изображения, которое движок слияния почты должен вставить в документ. |
| [set_ImageHeight](./set_imageheight/)(const System::SharedPtr\<Aspose::Words::Fields::MergeFieldImageDimension\>\&) | Сеттер для [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_ImageHeight](./get_imageheight/). |
| [set_ImageStream](./set_imagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Указывает поток, из которого движок слияния почты будет считывать изображение. |
| [set_ImageStream](./set_imagestream/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [set_ImageWidth](./set_imagewidth/)(const System::SharedPtr\<Aspose::Words::Fields::MergeFieldImageDimension\>\&) | Сеттер для [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_ImageWidth](./get_imagewidth/). |
| [set_Shape](./set_shape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | Сеттер для [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape](./get_shape/). |
| static [Type](./type/)() |  |
## Примечания


Это событие происходит во время слияния почты, когда в документе встречается поле слияния изображения. Вы можете обработать это событие, чтобы вернуть имя файла, поток или объект **Image** движку слияния почты, чтобы он был вставлен в документ.

Доступны три свойства [ImageFileName](./get_imagefilename/), [ImageStream](./get_imagestream/) и [Image](./get_image/), позволяющие указать, откуда брать изображение. Устанавливайте только одно из этих свойств.

Чтобы вставить поле слияния изображения в документ Word, выберите команду Вставка/Поле, затем выберите MergeField и введите Image:MyFieldName.

## См. также

* Class [FieldMergingArgsBase](../fieldmergingargsbase/)
* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
