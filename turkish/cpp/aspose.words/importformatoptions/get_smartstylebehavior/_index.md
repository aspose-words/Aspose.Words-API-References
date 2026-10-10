---
title: "Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior yöntemi"
linktitle: "get_SmartStyleBehavior"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior yöntemi. Kaynak ve hedef belgelerde aynı ada sahip stillerin nasıl içe aktarılacağını belirten bir boolean değer alır veya ayarlar. Varsayılan değer C++'ta false'tur."
type: docs
weight: 9000
url: /tr/cpp/aspose.words/importformatoptions/get_smartstylebehavior/
---
## ImportFormatOptions::get_SmartStyleBehavior method


Kaynak ve hedef belgelerde aynı ada sahip stillerin nasıl içe aktarılacağını belirten bir boolean değer alır veya ayarlar. Varsayılan değer **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior() const
```

## Açıklamalar


Bu seçenek **etkin** olduğunda, [KeepSourceFormatting](../../importformatmode/) içe aktarma modu kullanılıyorsa, kaynak stil hedef belge içinde doğrudan özniteliklere genişletilecektir.

Bu seçenek **devre dışı** olduğunda, kaynak stil yalnızca numaralandırılmışsa genişletilecektir. Mevcut hedef öznitelikler, listeler dahil, üzerine yazılmayacaktır.

## Örnekler



Belgeleri eklerken yinelenen stilleri nasıl çözeceğini gösterir.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);

System::SharedPtr<Aspose::Words::Style> myStyle = builder->get_Document()->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
myStyle->get_Font()->set_Size(14);
myStyle->get_Font()->set_Name(u"Courier New");
myStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

builder->get_ParagraphFormat()->set_StyleName(myStyle->get_Name());
builder->Writeln(u"Hello world!");

// Belgeyi klonlayın ve klonun "MyStyle" stilini düzenleyin, böylece orijinalinkinden farklı bir renge sahip olur.
// Klonu orijinal belgeye eklerseniz, aynı ada sahip iki stil çakışmaya neden olur.
System::SharedPtr<Aspose::Words::Document> srcDoc = dstDoc->Clone();
srcDoc->get_Styles()->idx_get(u"MyStyle")->get_Font()->set_Color(System::Drawing::Color::get_Red());

// SmartStyleBehavior'ı etkinleştirdiğimizde ve KeepSourceFormatting içe aktarma biçim modunu kullandığımızda,
// Aspose.Words, kaynak belge stillerini dönüştürerek stil çakışmalarını çözecektir.
// hedef stillerle aynı isimlere sahip olanları doğrudan paragraf özniteliklerine dönüştürerek.
auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_SmartStyleBehavior(true);

builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.SmartStyleBehavior.docx");
```

## Ayrıca Bakınız

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
