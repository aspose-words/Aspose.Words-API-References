---
title: "Метод Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix"
linktitle: "get_CssClassNamePrefix"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix. Указывает префикс, который добавляется ко всем именам CSS‑классов. Значение по умолчанию — пустая строка, и сгенерированные имена CSS‑классов не имеют общего префикса в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_cssclassnameprefix/
---
## HtmlSaveOptions::get_CssClassNamePrefix method


Указывает префикс, который добавляется ко всем именам CSS‑классов. Значение по умолчанию — пустая строка, и сгенерированные имена CSS‑классов не имеют общего префикса.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix() const
```

## Примечания


Если это значение не пусто, все CSS‑классы, генерируемые Aspose.Words, будут начинаться с указанного префикса. Это может быть полезно, например, если вы добавляете пользовательский CSS к сгенерированным документам и хотите избежать конфликтов имён классов.

Если значение не **null** и не пусто, оно должно быть действительным идентификатором CSS.

## Примеры



Показывает, как сохранить документ в HTML и добавить префикс ко всем его именам CSS‑классов.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::External);
saveOptions->set_CssClassNamePrefix(u"myprefix-");

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.CssClassNamePrefix.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.CssClassNamePrefix.html");

ASSERT_TRUE(outDocContents.Contains(u"<p class=\"myprefix-Header\">"));
ASSERT_TRUE(outDocContents.Contains(u"<p class=\"myprefix-Footer\">"));

outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.CssClassNamePrefix.css");

ASSERT_TRUE(outDocContents.Contains(u".myprefix-Footer { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:footer }"));
ASSERT_TRUE(outDocContents.Contains(u".myprefix-Header { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:header }"));
```

## См. также

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
