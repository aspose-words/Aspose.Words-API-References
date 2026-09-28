---
title: "Aspose::Words::ParagraphFormat::get_MirrorIndents метод"
linktitle: "get_MirrorIndents"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::ParagraphFormat::get_MirrorIndents. Получает или задает флаг, указывающий, одинаковы ли левый и правый отступы по ширине в C++."
type: docs
weight: 24500
url: /ru/cpp/aspose.words/paragraphformat/get_mirrorindents/
---
## ParagraphFormat::get_MirrorIndents method


Получает или задает флаг, указывающий, одинаковой ли ширины левый и правый отступы.

```cpp
bool Aspose::Words::ParagraphFormat::get_MirrorIndents()
```


## Примеры



Показать, как сделать левый и правый отступы одинаковыми.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat();

format->set_MirrorIndents(true);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.MirrorIndents.docx");
```

## См. также

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
