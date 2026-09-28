---
title: "Aspose::Words::Drawing::SignatureLine::get_Signer метод"
linktitle: "get_Signer"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::SignatureLine::get_Signer метод. Получает или задает предложенного подписанта строки подписи. Значение по умолчанию для этого свойства — пустая строка в C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words.drawing/signatureline/get_signer/
---
## SignatureLine::get_Signer method


Получает или задает предложенного подписанта строки подписи. Значение по умолчанию для этого свойства — **empty string**.

```cpp
System::String Aspose::Words::Drawing::SignatureLine::get_Signer()
```


## Примеры



Показывает, как создать строку подписи и вставить её в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto options = System::MakeObject<Aspose::Words::SignatureLineOptions>();
options->set_AllowComments(true);
options->set_DefaultInstructions(true);
options->set_Email(u"john.doe@management.com");
options->set_Instructions(u"Please sign here");
options->set_ShowDate(true);
options->set_Signer(u"John Doe");
options->set_SignerTitle(u"Senior Manager");

// Вставьте форму, которая будет содержать строку подписи, внешний вид которой мы будем
// настраивать с помощью объекта "SignatureLineOptions", который мы создали выше.
// Если мы вставим форму, координаты которой начинаются в правом нижнем углу страницы,
// нам понадобится задать отрицательные координаты x и y, чтобы форма стала видимой.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertSignatureLine(options, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, -170.0, Aspose::Words::Drawing::RelativeVerticalPosition::BottomMargin, -60.0, Aspose::Words::Drawing::WrapType::None);

ASSERT_TRUE(shape->get_IsSignatureLine());

// Проверьте свойства нашей строки подписи через её объект Shape.
System::SharedPtr<Aspose::Words::Drawing::SignatureLine> signatureLine = shape->get_SignatureLine();

ASSERT_EQ(u"john.doe@management.com", signatureLine->get_Email());
ASSERT_EQ(u"John Doe", signatureLine->get_Signer());
ASSERT_EQ(u"Senior Manager", signatureLine->get_SignerTitle());
ASSERT_EQ(u"Please sign here", signatureLine->get_Instructions());
ASSERT_TRUE(signatureLine->get_ShowDate());
ASSERT_TRUE(signatureLine->get_AllowComments());
ASSERT_TRUE(signatureLine->get_DefaultInstructions());

doc->Save(get_ArtifactsDir() + u"Shape.SignatureLine.docx");
```

## См. также

* Class [SignatureLine](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
