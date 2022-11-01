---
title: get_SimplifyListLabels
second_title: Aspose.Words for C++ API Reference
description: Specifies whether the program should simplify list labels in case of complex label formatting not being adequately represented by plain text. If set to true, numbered list labels are written in simple numeric format and itemized list labels as simple ASCII characters. The default value is false.
type: docs
weight: 79
url: /cpp/aspose.words.saving/txtsaveoptions/get_simplifylistlabels/
---
## TxtSaveOptions.get_SimplifyListLabels method


Specifies whether the program should simplify list labels in case of complex label formatting not being adequately represented by plain text. If set to **true**, numbered list labels are written in simple numeric format and itemized list labels as simple ASCII characters. The default value is **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptions::get_SimplifyListLabels() const
```


## Examples




Shows how to change the appearance of lists when saving a document to plaintext. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Create a bulleted list with five levels of indentation.
builder->get_ListFormat()->ApplyBulletDefault();
builder->Writeln(u"Item 1");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 2");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 3");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 4");
builder->get_ListFormat()->ListIndent();
builder->Write(u"Item 5");

// Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
// to modify how we save the document to plaintext.
auto txtSaveOptions = MakeObject<TxtSaveOptions>();

// Set the "SimplifyListLabels" property to "true" to convert some list
// symbols into simpler ASCII characters, such as '*', 'o', '+', '>', etc.
// Set the "SimplifyListLabels" property to "false" to preserve as many original list symbols as possible.
txtSaveOptions->set_SimplifyListLabels(simplifyListLabels);

doc->Save(ArtifactsDir + u"TxtSaveOptions.SimplifyListLabels.txt", txtSaveOptions);

String docText = System::IO::File::ReadAllText(ArtifactsDir + u"TxtSaveOptions.SimplifyListLabels.txt");

if (simplifyListLabels)
{
    ASSERT_EQ(String(u"* Item 1\r\n") + u"  > Item 2\r\n" + u"    + Item 3\r\n" + u"      - Item 4\r\n" + u"        o Item 5\r\n", docText);
}
else
{
    ASSERT_EQ(String(u"· Item 1\r\n") + u"o Item 2\r\n" + u"§ Item 3\r\n" + u"· Item 4\r\n" + u"o Item 5\r\n", docText);
}
```

