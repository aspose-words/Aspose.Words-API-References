---
title: "Aspose::Words::Drawing::TextBoxAnchor enum"
linktitle: "TextBoxAnchor"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::TextBoxAnchor enum. Şekil metninin dikey hizalaması için C++'da kullanılan değerleri belirtir."
type: docs
weight: 39000
url: /tr/cpp/aspose.words.drawing/textboxanchor/
---
## TextBoxAnchor enum


Şekil metninin dikey hizalaması için kullanılan değerleri belirtir.

```cpp
enum class TextBoxAnchor
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Üst | 0 | Metin metin kutusunun üst kısmına hizalanır. |
| Orta | 1 | Metin metin kutusunun ortasına hizalanır. |
| Alt | 2 | Metin metin kutusunun altına hizalanır. |
| TopCentered | 3 | Metin metin kutusunun üst ortasına hizalanır. |
| MiddleCentered | 4 | Metin metin kutusunun orta ortasına hizalanır. |
| BottomCentered | 5 | Metin metin kutusunun alt ortasına hizalanır. |
| TopBaseline | 6 | Metin metin kutusunun üst taban çizgisine hizalanır. |
| BottomBaseline | 7 | Metin metin kutusunun alt taban çizgisine hizalanır. |
| TopCenteredBaseline | 8 | Metin, metin kutusunun üst ortalanmış taban çizgisine hizalanır. |
| BottomCenteredBaseline | 9 | Metin, metin kutusunun alt ortalanmış taban çizgisine hizalanır. |


## Örnekler



Bir metin kutusunun metin içeriğini dikey olarak nasıl hizalayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 200, 200);

// \"VerticalAnchor\" özelliğini \"TextBoxAnchor.Top\" olarak ayarlayın
// bu metin kutusundaki metni şeklin üst tarafına hizalayın.
// \"VerticalAnchor\" özelliğini \"TextBoxAnchor.Middle\" olarak ayarlayın
// bu metin kutusundaki metni şeklin ortasına hizalayın.
// \"VerticalAnchor\" özelliğini \"TextBoxAnchor.Bottom\" olarak ayarlayın
// bu metin kutusundaki metni şeklin altına hizalayın.
shape->get_TextBox()->set_VerticalAnchor(verticalAnchor);

builder->MoveTo(shape->get_FirstParagraph());
builder->Write(u"Hello world!");

// Metin kutularının içindeki metnin dikey hizalanması Microsoft Word 2007 ve sonrasında kullanılabilir.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2007);
doc->Save(get_ArtifactsDir() + u"Shape.VerticalAnchor.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
