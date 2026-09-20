---
title: "Метод Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags"
linktitle: "get_IgnoreStructuredDocumentTags"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags метод. Получает или задает логическое значение, указывающее, следует ли игнорировать содержимое StructuredDocumentTag. Значение по умолчанию — false в C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words.replacing/findreplaceoptions/get_ignorestructureddocumenttags/
---
## FindReplaceOptions::get_IgnoreStructuredDocumentTags method


Получает или задает логическое значение, указывающее, следует ли игнорировать содержимое [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/). Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags() const
```

## Примечания


Когда эта опция установлена в **true**, содержимое [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) будет рассматриваться как простой текст.

В противном случае, [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) будет обрабатываться как отдельный [Story](../../../aspose.words/story/) и шаблон замены будет искаться отдельно для каждого [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/), так что если шаблон пересекает [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/), замена для такого шаблона не будет выполнена.

## Примеры



Показывает, как игнорировать содержимое тегов при замене.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// Этот абзац содержит SDT.
auto p = System::ExplicitCast<Aspose::Words::Paragraph>(doc->get_FirstSection()->get_Body()->GetChild(Aspose::Words::NodeType::Paragraph, 2, true));
System::String textToSearch = p->ToString(Aspose::Words::SaveFormat::Text).Trim();

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreStructuredDocumentTags(true);
doc->get_Range()->Replace(textToSearch, u"replacement", options);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.IgnoreStructuredDocumentTags.docx");
```

## См. также

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
