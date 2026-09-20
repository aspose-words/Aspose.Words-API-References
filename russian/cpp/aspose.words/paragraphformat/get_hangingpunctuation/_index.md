---
title: "Aspose::Words::ParagraphFormat::get_HangingPunctuation метод"
linktitle: "get_HangingPunctuation"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ParagraphFormat::get_HangingPunctuation метод. Получает или задает флаг, указывающий, включена ли висячая пунктуация для текущего абзаца в C++."
type: docs
weight: 14000
url: /ru/cpp/aspose.words/paragraphformat/get_hangingpunctuation/
---
## ParagraphFormat::get_HangingPunctuation method


Получает или задает флаг, указывающий, включена ли висячая пунктуация для текущего абзаца.

```cpp
bool Aspose::Words::ParagraphFormat::get_HangingPunctuation()
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
