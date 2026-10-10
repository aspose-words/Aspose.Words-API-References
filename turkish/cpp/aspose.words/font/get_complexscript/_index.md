---
title: "Aspose::Words::Font::get_ComplexScript yöntemi"
linktitle: "get_ComplexScript"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_ComplexScript yöntemi. Bu koşunun içeriğinin, C++'ta bu koşunun biçimlendirmesini belirlerken Unicode karakter değerlerinden bağımsız olarak karmaşık betik metni olarak işlenip işlenmeyeceğini belirtir."
type: docs
weight: 10000
url: /tr/cpp/aspose.words/font/get_complexscript/
---
## Font::get_ComplexScript method


Bu çalışmanın biçimlendirmesini belirlerken, içeriğin Unicode karakter değerlerinden bağımsız olarak karmaşık betik metni olarak ele alınıp alınmayacağını belirtir.

```cpp
bool Aspose::Words::Font::get_ComplexScript()
```


## Örnekler



Her zaman karmaşık betik olarak işlenen metin eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_ComplexScript(true);

builder->Writeln(u"Text treated as complex script.");

doc->Save(get_ArtifactsDir() + u"Font.ComplexScript.docx");
```

## Ayrıca Bakınız

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
