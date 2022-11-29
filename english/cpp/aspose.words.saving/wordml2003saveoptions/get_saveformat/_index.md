---
title: get_SaveFormat
second_title: Aspose.Words for C++ API Reference
description: Specifies the format in which the document will be saved if this save options object is used. Can only be WordML.
type: docs
weight: 1
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Create a "WordML2003SaveOptions" object to pass to the document's "Save" method
// to modify how we save the document to the WordML save format.
auto options = MakeObject<WordML2003SaveOptions>();

ASSERT_EQ(SaveFormat::WordML, options->get_SaveFormat());

// Set the "PrettyFormat" property to "true" to apply tab character indentation and
// newlines to make the output document's raw content easier to read.
// Set the "PrettyFormat" property to "false" to save the document's raw content in one continuous body of the text.
options->set_PrettyFormat(prettyFormat);

doc->Save(ArtifactsDir + u"WordML2003SaveOptions.PrettyFormat.xml", options);

String fileContents = System::IO::File::ReadAllText(ArtifactsDir + u"WordML2003SaveOptions.PrettyFormat.xml");

if (prettyFormat)
{
    ASSERT_TRUE(fileContents.Contains(String(u"<o:DocumentProperties>\r\n\t\t") + u"<o:Revision>1</o:Revision>\r\n\t\t" +
                                      u"<o:TotalTime>0</o:TotalTime>\r\n\t\t" + u"<o:Pages>1</o:Pages>\r\n\t\t" + u"<o:Words>0</o:Words>\r\n\t\t" +
                                      u"<o:Characters>0</o:Characters>\r\n\t\t" + u"<o:Lines>1</o:Lines>\r\n\t\t" +
                                      u"<o:Paragraphs>1</o:Paragraphs>\r\n\t\t" + u"<o:CharactersWithSpaces>0</o:CharactersWithSpaces>\r\n\t\t" +
                                      u"<o:Version>11.5606</o:Version>\r\n\t" + u"</o:DocumentProperties>"));
}
else
{
    ASSERT_TRUE(fileContents.Contains(String(u"<o:DocumentProperties><o:Revision>1</o:Revision><o:TotalTime>0</o:TotalTime><o:Pages>1</o:Pages>") +
                                      u"<o:Words>0</o:Words><o:Characters>0</o:Characters><o:Lines>1</o:Lines><o:Paragraphs>1</o:Paragraphs>" +
                                      u"<o:CharactersWithSpaces>0</o:CharactersWithSpaces><o:Version>11.5606</o:Version></o:DocumentProperties>"));
}
```

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [WordML2003SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
