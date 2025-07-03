---
title: Aspose::Words::Saving::HtmlSaveOptions::get_ReplaceBackslashWithYenSign method
linktitle: get_ReplaceBackslashWithYenSign
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlSaveOptions::get_ReplaceBackslashWithYenSign method. Specifies whether backslash characters should be replaced with yen signs. Default value is false in C++.'
type: docs
weight: 41500
url: /cpp/aspose.words.saving/htmlsaveoptions/get_replacebackslashwithyensign/
---
## HtmlSaveOptions::get_ReplaceBackslashWithYenSign method


Specifies whether backslash characters should be replaced with yen signs. Default value is **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ReplaceBackslashWithYenSign() const
```


## Examples



Shows how to replace backslash characters with yen signs (Html). 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Korean backslash symbol.docx");

// By default, Aspose.Words mimics MS Word's behavior and doesn't replace backslash characters with yen signs in
// generated HTML documents. However, previous versions of Aspose.Words performed such replacements in certain
// scenarios. This flag enables backward compatibility with previous versions of Aspose.Words.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_ReplaceBackslashWithYenSign(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ReplaceBackslashWithYenSign.html", saveOptions);
```

## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
