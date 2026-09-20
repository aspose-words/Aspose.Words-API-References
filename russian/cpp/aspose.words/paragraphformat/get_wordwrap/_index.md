---
title: "Метод Aspose::Words::ParagraphFormat::get_WordWrap"
linktitle: "get_WordWrap"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::ParagraphFormat::get_WordWrap. Если это свойство ложно, латинский текст в середине слова может переноситься в текущем абзаце. В противном случае латинский текст переносится целыми словами в C++."
type: docs
weight: 42000
url: /ru/cpp/aspose.words/paragraphformat/get_wordwrap/
---
## ParagraphFormat::get_WordWrap method


Если это свойство имеет значение **false**, латинский текст в середине слова может переноситься в текущем абзаце. В противном случае латинский текст переносится целыми словами.

```cpp
bool Aspose::Words::ParagraphFormat::get_WordWrap()
```


## Примеры



Показывает, как задать специальные свойства для азиатской типографии.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();
format->set_FarEastLineBreakControl(true);
format->set_WordWrap(false);
format->set_HangingPunctuation(true);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.AsianTypographyProperties.docx");
```

## См. также

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
