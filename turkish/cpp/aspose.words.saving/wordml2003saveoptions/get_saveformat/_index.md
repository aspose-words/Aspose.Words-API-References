---
title: "Aspose::Words::Saving::WordML2003SaveOptions::get_SaveFormat yöntemi"
linktitle: "get_SaveFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::WordML2003SaveOptions::get_SaveFormat yöntemi. Bu kaydetme seçenekleri nesnesi kullanıldığında belgenin kaydedileceği formatı belirtir. C++'ta yalnızca WordML olabilir."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.saving/wordml2003saveoptions/get_saveformat/
---
## WordML2003SaveOptions::get_SaveFormat method


Bu kaydetme seçenekleri nesnesi kullanıldığında belgenin kaydedileceği formatı belirtir. Yalnızca [WordML](../../../aspose.words/saveformat/) olabilir.

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::WordML2003SaveOptions::get_SaveFormat() override
```


## Örnekler



Çıktı belgesinin ham içeriğini nasıl yöneteceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// "WordML2003SaveOptions" nesnesi oluşturun ve belgeye ait "Save" yöntemine geçirin
// belgeyi WordML kaydetme formatına nasıl kaydedeceğimizi değiştirmek için.
auto options = System::MakeObject<Aspose::Words::Saving::WordML2003SaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::WordML, options->get_SaveFormat());

// "PrettyFormat" özelliğini "true" olarak ayarlayın, sekme karakteri girintisi ve
// yeni satırları ekleyerek çıktı belgesinin ham içeriğini daha kolay okunur hâle getirin.
// "PrettyFormat" özelliğini "false" olarak ayarlayın, belgenin ham içeriğini tek bir sürekli metin bloğu olarak kaydedin.
options->set_PrettyFormat(prettyFormat);

doc->Save(get_ArtifactsDir() + u"WordML2003SaveOptions.PrettyFormat.xml", options);

System::String fileContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"WordML2003SaveOptions.PrettyFormat.xml");
System::String newLine = System::Environment::get_NewLine();
if (prettyFormat)
{
    ASSERT_TRUE(fileContents.Contains(System::String::Format(u"<o:DocumentProperties>{0}\t\t", newLine) + System::String::Format(u"<o:Revision>1</o:Revision>{0}\t\t", newLine) + System::String::Format(u"<o:TotalTime>0</o:TotalTime>{0}\t\t", newLine) + System::String::Format(u"<o:Pages>1</o:Pages>{0}\t\t", newLine) + System::String::Format(u"<o:Words>0</o:Words>{0}\t\t", newLine) + System::String::Format(u"<o:Characters>0</o:Characters>{0}\t\t", newLine) + System::String::Format(u"<o:Lines>1</o:Lines>{0}\t\t", newLine) + System::String::Format(u"<o:Paragraphs>1</o:Paragraphs>{0}\t\t", newLine) + System::String::Format(u"<o:CharactersWithSpaces>0</o:CharactersWithSpaces>{0}\t\t", newLine) + System::String::Format(u"<o:Version>11.5606</o:Version>{0}\t", newLine) + u"</o:DocumentProperties>"));
}
else
{
    ASSERT_TRUE(fileContents.Contains(System::String(u"<o:DocumentProperties><o:Revision>1</o:Revision><o:TotalTime>0</o:TotalTime><o:Pages>1</o:Pages>") + u"<o:Words>0</o:Words><o:Characters>0</o:Characters><o:Lines>1</o:Lines><o:Paragraphs>1</o:Paragraphs>" + u"<o:CharactersWithSpaces>0</o:CharactersWithSpaces><o:Version>11.5606</o:Version></o:DocumentProperties>"));
}
```

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [WordML2003SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
