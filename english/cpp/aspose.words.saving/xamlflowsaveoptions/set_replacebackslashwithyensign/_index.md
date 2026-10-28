---
title: Aspose::Words::Saving::XamlFlowSaveOptions::set_ReplaceBackslashWithYenSign method
linktitle: set_ReplaceBackslashWithYenSign
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::XamlFlowSaveOptions::set_ReplaceBackslashWithYenSign method. Specifies whether backslash characters should be replaced with yen signs. Default value is false in C++.'
type: docs
weight: 11500
url: /cpp/aspose.words.saving/xamlflowsaveoptions/set_replacebackslashwithyensign/
---
## XamlFlowSaveOptions::set_ReplaceBackslashWithYenSign method


Specifies whether backslash characters should be replaced with yen signs. Default value is **false**.

```cpp
void Aspose::Words::Saving::XamlFlowSaveOptions::set_ReplaceBackslashWithYenSign(bool value)
```

## Remarks

 By default, Aspose.Words mimics MS Word's behavior and doesn't replace backslash characters with yen signs in generated XAML documents. However, previous versions of Aspose.Words performed such replacements in certain scenarios. This flag enables backward compatibility with previous versions of Aspose.Words. 
## Examples


Shows how to replace backslash characters with yen signs (Xaml).

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Korean backslash symbol.docx"));

// By default, Aspose.Words mimics MS Word's behavior and doesn't replace backslash characters with yen signs in
// generated HTML documents. However, previous versions of Aspose.Words performed such replacements in certain
// scenarios. This flag enables backward compatibility with previous versions of Aspose.Words.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::XamlFlowSaveOptions>();
saveOptions->set_ReplaceBackslashWithYenSign(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ReplaceBackslashWithYenSign.xaml", saveOptions);
```
## See Also

* Class [XamlFlowSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
