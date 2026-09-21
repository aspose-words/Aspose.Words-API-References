---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ReplaceBackslashWithYenSign method"
linktitle: "get_ReplaceBackslashWithYenSign"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ReplaceBackslashWithYenSign method. Anger om bakstrecks‑tecken ska ersättas med yen‑tecken. Standardvärdet är false i C++."
type: docs
weight: 41500
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_replacebackslashwithyensign/
---
## HtmlSaveOptions::get_ReplaceBackslashWithYenSign method


Anger om bakstrecks-tecken ska ersättas med yen-tecken. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ReplaceBackslashWithYenSign() const
```


## Exempel



Visar hur man ersätter bakstrecks‑tecken med yen‑tecken (Html).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Korean backslash symbol.docx");

// Som standard efterliknar Aspose.Words MS Words beteende och ersätter inte bakstrecks‑tecken med yen‑tecken i
// genererade HTML-dokument. Dock utförde tidigare versioner av Aspose.Words sådana ersättningar i vissa
// scenarier. Denna flagga möjliggör bakåtkompatibilitet med tidigare versioner av Aspose.Words.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_ReplaceBackslashWithYenSign(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ReplaceBackslashWithYenSign.html", saveOptions);
```

## Se även

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
