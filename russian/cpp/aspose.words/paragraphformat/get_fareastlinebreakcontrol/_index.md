---
title: "Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl method"
linktitle: "get_FarEastLineBreakControl"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl method. Получает или задает флаг, указывающий, применяются ли правила разрыва строк для восточноазиатских языков к текущему абзацу в C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words/paragraphformat/get_fareastlinebreakcontrol/
---
## ParagraphFormat::get_FarEastLineBreakControl method


Получает или задает флаг, указывающий, применяются ли правила разрыва строк для восточноазиатского текста к текущему абзацу.

```cpp
bool Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl()
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
