---
title: "Метод Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks"
linktitle: "get_RemoveJavaScriptFromLinks"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks. Указывает, будет ли JavaScript удалён из ссылок. По умолчанию false. Если эта опция включена, все ссылки, содержащие JavaScript, будут заменены на \"javascript:void(0)\" в C++."
type: docs
weight: 4750
url: /ru/cpp/aspose.words.saving/svgsaveoptions/get_removejavascriptfromlinks/
---
## SvgSaveOptions::get_RemoveJavaScriptFromLinks method


Указывает, будет ли JavaScript удалён из ссылок. По умолчанию **false**. Если эта опция включена, все ссылки, содержащие JavaScript, будут заменены на "javascript:void(0)".

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks() const
```


## Примеры



Показывает, как удалить JavaScript из ссылок (svg).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"JavaScript in HREF.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_RemoveJavaScriptFromLinks(true);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.RemoveJavaScriptFromLinksSvg.html", saveOptions);
```

## См. также

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
