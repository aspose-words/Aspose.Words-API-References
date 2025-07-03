---
title: Aspose::Words::ImportFormatOptions::get_ForceCopyStyles method
linktitle: get_ForceCopyStyles
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ImportFormatOptions::get_ForceCopyStyles method. Gets or sets a boolean value indicating either to copy conflicting styles in KeepSourceFormatting mode. The default value is false in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words/importformatoptions/get_forcecopystyles/
---
## ImportFormatOptions::get_ForceCopyStyles method


Gets or sets a boolean value indicating either to copy conflicting styles in [KeepSourceFormatting](../../importformatmode/) mode. The default value is **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_ForceCopyStyles() const
```

## Remarks


By default, if a matching style already exists in a destination document, the source style formatting is expanded into direct node attributes and the style of this node is reset to a default.

When this option is set to **true**, the source style will be forcibly copied into destination document with unique name and applied to the imported node.

Note, in this case it is not guaranteed that formatting of the imported node in destination document will be preserved.

## Examples



Shows how to copy source styles with unique names forcibly. 
```cpp
// Both documents contain MyStyle1 and MyStyle2, MyStyle3 exists only in a source document.
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Styles source.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Styles destination.docx");

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ForceCopyStyles(true);
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

System::SharedPtr<Aspose::Words::ParagraphCollection> paras = dstDoc->get_Sections()->idx_get(1)->get_Body()->get_Paragraphs();

ASSERT_EQ(paras->idx_get(0)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle1_0");
ASSERT_EQ(paras->idx_get(1)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle2_0");
ASSERT_EQ(paras->idx_get(2)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle3");
```

## See Also

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
