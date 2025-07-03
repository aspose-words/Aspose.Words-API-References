---
title: Aspose::Words::Saving::WordML2003SaveOptions::get_SaveFormat method
linktitle: get_SaveFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::WordML2003SaveOptions::get_SaveFormat method. Specifies the format in which the document will be saved if this save options object is used. Can only be WordML in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.saving/wordml2003saveoptions/get_saveformat/
---
## WordML2003SaveOptions::get_SaveFormat method


Specifies the format in which the document will be saved if this save options object is used. Can only be [WordML](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::WordML2003SaveOptions::get_SaveFormat() override
```


## Examples



Shows how to manage output document's raw content. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Create a "WordML2003SaveOptions" object to pass to the document's "Save" method
// to modify how we save the document to the WordML save format.
auto options = System::MakeObject<Aspose::Words::Saving::WordML2003SaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::WordML, options->get_SaveFormat());

// Set the "PrettyFormat" property to "true" to apply tab character indentation and
// newlines to make the output document's raw content easier to read.
// Set the "PrettyFormat" property to "false" to save the document's raw content in one continuous body of the text.
options->set_PrettyFormat(prettyFormat);

doc->Save(get_ArtifactsDir() + u"WordML2003SaveOptions.PrettyFormat.xml", options);

System::String fileContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"WordML2003SaveOptions.PrettyFormat.xml");

if (prettyFormat)
{
    ASSERT_TRUE(fileContents.Contains(System::String(u"<o:DocumentProperties>\r\n\t\t") + u"<o:Revision>1</o:Revision>\r\n\t\t" + u"<o:TotalTime>0</o:TotalTime>\r\n\t\t" + u"<o:Pages>1</o:Pages>\r\n\t\t" + u"<o:Words>0</o:Words>\r\n\t\t" + u"<o:Characters>0</o:Characters>\r\n\t\t" + u"<o:Lines>1</o:Lines>\r\n\t\t" + u"<o:Paragraphs>1</o:Paragraphs>\r\n\t\t" + u"<o:CharactersWithSpaces>0</o:CharactersWithSpaces>\r\n\t\t" + u"<o:Version>11.5606</o:Version>\r\n\t" + u"</o:DocumentProperties>"));
}
else
{
    ASSERT_TRUE(fileContents.Contains(System::String(u"<o:DocumentProperties><o:Revision>1</o:Revision><o:TotalTime>0</o:TotalTime><o:Pages>1</o:Pages>") + u"<o:Words>0</o:Words><o:Characters>0</o:Characters><o:Lines>1</o:Lines><o:Paragraphs>1</o:Paragraphs>" + u"<o:CharactersWithSpaces>0</o:CharactersWithSpaces><o:Version>11.5606</o:Version></o:DocumentProperties>"));
}
```

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [WordML2003SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
