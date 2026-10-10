---
title: "Aspose::Words::Saving::TxtSaveOptions::get_SaveFormat method"
linktitle: "get_SaveFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::TxtSaveOptions::get_SaveFormat yöntemi. Bu kaydetme seçenekleri nesnesi kullanıldığında belgenin hangi formatta kaydedileceğini belirtir. C++'ta yalnızca Text olabilir."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.saving/txtsaveoptions/get_saveformat/
---
## TxtSaveOptions::get_SaveFormat method


Bu kaydetme seçenekleri nesnesi kullanıldığında belgenin kaydedileceği formatı belirtir. Yalnızca [Text](../../../aspose.words/saveformat/) olabilir.

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::TxtSaveOptions::get_SaveFormat() override
```


## Örnekler



Özel bir paragraf sonu ile .txt belgesinin nasıl kaydedileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");
builder->Write(u"Paragraph 3.");

// Bir "TxtSaveOptions" nesnesi oluşturun, bunu belgenin "Save" yöntemine aktarabiliriz
// belgeyi düz metne kaydetme şeklini değiştirmek için.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Text, txtSaveOptions->get_SaveFormat());

// "ParagraphBreak" özelliğini her paragrafın sonuna koymak istediğimiz özel bir değere ayarlayın.
txtSaveOptions->set_ParagraphBreak(u" End of paragraph.\n\n\t");

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.ParagraphBreak.txt");

ASSERT_EQ(System::String(u"Paragraph 1. End of paragraph.\n\n\t") + u"Paragraph 2. End of paragraph.\n\n\t" + u"Paragraph 3. End of paragraph.\n\n\t", docText);
```

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
