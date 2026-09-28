---
title: "Метод Aspose::Words::Framesets::Frameset::get_IsFrameLinkToFile"
linktitle: "get_IsFrameLinkToFile"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Framesets::Frameset::get_IsFrameLinkToFile. Получает или задает значение, указывающее, является ли веб‑страница или имя файла документа, указанные в свойстве FrameDefaultUrl, внешним ресурсом, с которым связан кадр, в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.framesets/frameset/get_isframelinktofile/
---
## Frameset::get_IsFrameLinkToFile method


Получает или задает значение, указывающее, является ли веб‑страница или имя файла документа, указанные в свойстве [FrameDefaultUrl](../get_framedefaulturl/), внешним ресурсом, с которым связан кадр.

```cpp
bool Aspose::Words::Framesets::Frameset::get_IsFrameLinkToFile()
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

* Class [Frameset](../)
* Namespace [Aspose::Words::Framesets](../../)
* Library [Aspose.Words for C++](../../../)
