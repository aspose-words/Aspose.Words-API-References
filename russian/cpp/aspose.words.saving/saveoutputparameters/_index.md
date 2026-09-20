---
title: "Класс Aspose::Words::Saving::SaveOutputParameters"
linktitle: "SaveOutputParameters"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Saving::SaveOutputParameters. Этот объект возвращается вызывающему после сохранения документа и содержит дополнительную информацию, которая была сгенерирована или вычислена во время операции сохранения. Вызывающий может использовать этот объект или игнорировать его. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 30000
url: /ru/cpp/aspose.words.saving/saveoutputparameters/
---
## SaveOutputParameters class


Этот объект возвращается вызывающему после сохранения документа и содержит дополнительную информацию, которая была сгенерирована или вычислена во время операции сохранения. Вызывающий может использовать этот объект или игнорировать его. Чтобы узнать больше, посетите статью документации [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class SaveOutputParameters : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_ContentType](./get_contenttype/)() const | Возвращает строку Content-Type (Internet Media Type), определяющую тип сохранённого документа. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Примеры



Показывает, как получить доступ к параметрам вывода операции сохранения документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// После сохранения документа мы можем получить доступ к типу Интернет‑медиа (MIME‑type) вновь созданного выходного документа.
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> parameters = doc->Save(get_ArtifactsDir() + u"Document.SaveOutputParameters.doc");

ASSERT_EQ(u"application/msword", parameters->get_ContentType());

// Это свойство меняется в зависимости от формата сохранения.
parameters = doc->Save(get_ArtifactsDir() + u"Document.SaveOutputParameters.pdf");

ASSERT_EQ(u"application/pdf", parameters->get_ContentType());
```

## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
