---
title: "Aspose::Words::Drawing::ShapeBase::get_HRef yöntemi"
linktitle: "get_HRef"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_HRef yöntemi. C++'de bir şekil için tam hiperlink adresini alır veya ayarlar."
type: docs
weight: 24000
url: /tr/cpp/aspose.words.drawing/shapebase/get_href/
---
## ShapeBase::get_HRef method


Bir şekil için tam hiperlink adresini alır veya ayarlar.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_HRef()
```

## Açıklamalar


Varsayılan değer boş bir dizedir.

Aşağıda bu özellik için geçerli değer örnekleri verilmiştir:

Tam URI: **https://www.aspose.com/**.

Tam dosya adı: **C:\\My Documents\\SalesReport.doc**.

Göreli URI: **%../../../resource.txt**

Göreli dosya adı: **%..\\My Documents\\SalesReport.doc**.

[Bookmark](../../../aspose.words/bookmark/) within another document: **https://www.aspose.com/Products/Default.aspx::Suites**

[Bookmark](../../../aspose.words/bookmark/) within this document: **%#BookmakName**.

## Örnekler



Bir resmi içeren ve aynı zamanda bir köprü olan şeklin nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_HRef(u"https://forum.aspose.com/");
shape->set_Target(u"New Window");
shape->set_ScreenTip(u"Aspose.Words Support Forums");

// Microsoft Word'de şekle Ctrl + sol tıklama yeni bir web tarayıcı penceresi açar
// ve bizi "HRef" özelliğindeki köprüye götürür.
doc->Save(get_ArtifactsDir() + u"Image.InsertImageWithHyperlink.docx");
```

## Ayrıca Bakınız

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
