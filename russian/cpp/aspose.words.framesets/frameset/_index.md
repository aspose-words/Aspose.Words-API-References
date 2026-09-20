---
title: "Aspose::Words::Framesets::Frameset class"
linktitle: "Frameset"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Framesets::Frameset class. Представляет страницу фреймов или отдельный фрейм на странице фреймов. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.framesets/frameset/
---
## Frameset class


Представляет страницу фреймов или отдельный фрейм на странице фреймов. Чтобы узнать больше, посетите статью документации [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class Frameset : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [Frameset](./frameset/)() |  |
| [get_ChildFramesets](./get_childframesets/)() const | Получает коллекцию дочерних фреймов и страниц фреймов. |
| [get_FrameDefaultUrl](./get_framedefaulturl/)() | Получает или задает URL веб-страницы или имя файла документа для отображения в этом фрейме. |
| [get_IsFrameLinkToFile](./get_isframelinktofile/)() | Получает или задает значение, указывающее, является ли веб-страница или имя файла документа, указанные в свойстве [FrameDefaultUrl](./get_framedefaulturl/), внешним ресурсом, с которым связан фрейм. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FrameDefaultUrl](./set_framedefaulturl/)(const System::String\&) | Сеттер для [Aspose::Words::Framesets::Frameset::get_FrameDefaultUrl](./get_framedefaulturl/). |
| [set_IsFrameLinkToFile](./set_isframelinktofile/)(bool) | Сеттер для [Aspose::Words::Framesets::Frameset::get_IsFrameLinkToFile](./get_isframelinktofile/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как получить доступ к фреймам на странице.
```cpp
// Документ содержит несколько фреймов со ссылками на другие документы.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Frameset.docx");

ASSERT_EQ(3, doc->get_Frameset()->get_ChildFramesets()->get_Count());
// Мы можем проверить URL по умолчанию (URL веб-страницы или локального документа) или является ли фрейм внешним ресурсом.
ASSERT_EQ(u"https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx", doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->get_FrameDefaultUrl());
ASSERT_TRUE(doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->get_IsFrameLinkToFile());

ASSERT_EQ(u"Document.docx", doc->get_Frameset()->get_ChildFramesets()->idx_get(1)->get_FrameDefaultUrl());
ASSERT_FALSE(doc->get_Frameset()->get_ChildFramesets()->idx_get(1)->get_IsFrameLinkToFile());

// Измените свойства одного из наших фреймов.
doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->set_FrameDefaultUrl(u"https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx");
doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->set_IsFrameLinkToFile(false);
```

## См. также

* Namespace [Aspose::Words::Framesets](../)
* Library [Aspose.Words for C++](../../)
