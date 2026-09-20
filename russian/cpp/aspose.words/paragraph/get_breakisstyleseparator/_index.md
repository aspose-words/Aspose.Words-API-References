---
title: "Метод Aspose::Words::Paragraph::get_BreakIsStyleSeparator"
linktitle: "get_BreakIsStyleSeparator"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Paragraph::get_BreakIsStyleSeparator. Возвращает true, если разрыв абзаца является разделителем стилей. Разделитель стилей позволяет одному абзацу состоять из частей с разными стилями абзацев в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words/paragraph/get_breakisstyleseparator/
---
## Paragraph::get_BreakIsStyleSeparator method


Возвращает true, если разрыв абзаца является разделителем [Style](../../style/). Разделитель стилей позволяет одному абзацу состоять из частей с разными стилями абзацев.

```cpp
bool Aspose::Words::Paragraph::get_BreakIsStyleSeparator()
```


## Примеры



Показывает, как записать текст в той же строке, что и заголовок оглавления, и чтобы он не отображался в оглавлении.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertTableOfContents(u"\\o \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Вставьте абзац со стилем, который будет распознан оглавлением как запись.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);

// Обе эти строки находятся в одном абзаце и поэтому будут отображаться в одной записи оглавления.
builder->Write(u"Heading 1. ");
builder->Write(u"Will appear in the TOC. ");

// Если вставить разделитель стилей, мы можем писать больше текста в том же абзаце
// и использовать другой стиль, не отображаясь в оглавлении.
// Если после разделителя использовать стиль заголовка, мы можем создать несколько записей оглавления из одной строки текста документа.
builder->InsertStyleSeparator();
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Quote);
builder->Write(u"Won't appear in the TOC. ");

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_BreakIsStyleSeparator());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Paragraph.BreakIsStyleSeparator.docx");
```

## См. также

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
