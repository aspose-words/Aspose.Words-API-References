---
title: "Aspose::Words::Framesets::FramesetCollection::get_Count метод"
linktitle: "get_Count"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Framesets::FramesetCollection::get_Count метод. Получает количество фреймов или страниц фреймов, содержащихся в коллекции, в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.framesets/framesetcollection/get_count/
---
## FramesetCollection::get_Count method


Получает количество фреймов или страниц фреймов, содержащихся в коллекции.

```cpp
int32_t Aspose::Words::Framesets::FramesetCollection::get_Count()
```


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

* Class [FramesetCollection](../)
* Namespace [Aspose::Words::Framesets](../../)
* Library [Aspose.Words for C++](../../../)
