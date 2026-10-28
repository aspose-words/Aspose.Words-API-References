---
title: Aspose::Words::ImportFormatOptions::set_ForceCopyStyles method
linktitle: set_ForceCopyStyles
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ImportFormatOptions::set_ForceCopyStyles method. Sets a boolean value indicating either to copy conflicting styles in KeepSourceFormatting mode. The default value is false in C++.'
type: docs
weight: 13000
url: /cpp/aspose.words/importformatoptions/set_forcecopystyles/
---
## ImportFormatOptions::set_ForceCopyStyles method


Sets a boolean value indicating either to copy conflicting styles in [KeepSourceFormatting](../../importformatmode/) mode. The default value is **false**.

```cpp
void Aspose::Words::ImportFormatOptions::set_ForceCopyStyles(bool value)
```

## Remarks


By default, if a matching style already exists in a destination document, the source style formatting is expanded into direct node attributes and the style of this node is reset to a default.

 When this option is set to **true**, the source style will be forcibly copied into destination document with unique name and applied to the imported node.

 Note, in this case it is not guaranteed that formatting of the imported node in destination document will be preserved. 
## Examples


Shows how to copy source styles with unique names forcibly.

```cpp
// Both documents contain MyStyle1 and MyStyle2, MyStyle3 exists only in a source document.
auto srcDoc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Styles source.docx"));
auto dstDoc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Styles destination.docx"));

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ForceCopyStyles(true);
dstDoc->AppendDocument(srcDoc, ImportFormatMode::KeepSourceFormatting, options);

System::SharedPtr<Aspose::Words::ParagraphCollection> paras = dstDoc->get_Sections()->idx_get(1)->get_Body()->get_Paragraphs();

ASSERT_EQ(paras->idx_get(0)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle1_0");
ASSERT_EQ(paras->idx_get(1)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle2_0");
ASSERT_EQ(paras->idx_get(2)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle3");
```
## See Also

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
