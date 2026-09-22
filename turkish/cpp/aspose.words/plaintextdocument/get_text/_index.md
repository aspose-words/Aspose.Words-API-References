---
title: "Aspose::Words::PlainTextDocument::get_Text yöntemi"
linktitle: "get_Text"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PlainTextDocument::get_Text yöntemi. Belgenin metin içeriğini bir dize olarak birleştirir ve C++'ta döndürür."
type: docs
weight: 5000
url: /tr/cpp/aspose.words/plaintextdocument/get_text/
---
## PlainTextDocument::get_Text method


Belgenin metinsel içeriğini bir dize olarak birleştirir.

```cpp
System::String Aspose::Words::PlainTextDocument::get_Text() const
```


## Örnekler



Bir Microsoft Word belgesinin içeriğini düz metin olarak yüklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
```

## Ayrıca Bakınız

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
