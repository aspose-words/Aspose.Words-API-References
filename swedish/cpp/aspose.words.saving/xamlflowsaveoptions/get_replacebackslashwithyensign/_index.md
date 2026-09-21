---
title: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ReplaceBackslashWithYenSign metod"
linktitle: "get_ReplaceBackslashWithYenSign"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ReplaceBackslashWithYenSign metod. Anger om bakstreck‑tecken ska ersättas med yen‑tecken. Standardvärdet är falskt i C++."
type: docs
weight: 5500
url: /sv/cpp/aspose.words.saving/xamlflowsaveoptions/get_replacebackslashwithyensign/
---
## XamlFlowSaveOptions::get_ReplaceBackslashWithYenSign method


Anger om bakstrecks-tecken ska ersättas med yen-tecken. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Saving::XamlFlowSaveOptions::get_ReplaceBackslashWithYenSign() const
```


## Exempel



Visar hur man ersätter bakstreck‑tecken med yen‑tecken (Xaml).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Korean backslash symbol.docx");

// Som standard efterliknar Aspose.Words MS Words beteende och ersätter inte bakstrecks‑tecken med yen‑tecken i
// genererade HTML-dokument. Dock utförde tidigare versioner av Aspose.Words sådana ersättningar i vissa
// scenarier. Denna flagga möjliggör bakåtkompatibilitet med tidigare versioner av Aspose.Words.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::XamlFlowSaveOptions>();
saveOptions->set_ReplaceBackslashWithYenSign(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ReplaceBackslashWithYenSign.xaml", saveOptions);
```

## Se även

* Class [XamlFlowSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
