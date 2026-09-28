---
title: "Aspose::Words::Drawing::SignatureLine class"
linktitle: "SignatureLine"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::SignatureLine class. Предоставляет доступ к свойствам строки подписи. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 13000
url: /ru/cpp/aspose.words.drawing/signatureline/
---
## SignatureLine class


Обеспечивает доступ к свойствам строки подписи. Чтобы узнать больше, посетите статью документации [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/) .

```cpp
class SignatureLine : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_AllowComments](./get_allowcomments/)() | Получает или задаёт значение, указывающее, что подписант может добавлять комментарии в диалоговом окне Sign. Значение свойства по умолчанию — **false**. |
| [get_DefaultInstructions](./get_defaultinstructions/)() | Получает или задает значение, указывающее, что стандартные инструкции отображаются в диалоговом окне подписи. Значение по умолчанию для этого свойства — **true**. |
| [get_Email](./get_email/)() | Получает или задает предложенный адрес электронной почты подписанта. Значение по умолчанию для этого свойства — **empty string**. |
| [get_Id](./get_id/)() | Получает или задаёт идентификатор этой строки подписи. Этот идентификатор может быть связан с цифровой подписью при подписании документа с помощью [DigitalSignatureUtil](../../aspose.words.digitalsignatures/digitalsignatureutil/). Это значение должно быть уникальным, и по умолчанию генерируется случайный новый Guid (**NewGuid**). |
| [get_Instructions](./get_instructions/)() | Получает или задает инструкции подписанту, которые отображаются при подписании строки подписи. Это свойство игнорируется, если установлен [DefaultInstructions](./get_defaultinstructions/). Значение по умолчанию для этого свойства — **empty string**. |
| [get_IsSigned](./get_issigned/)() | Указывает, что строка подписи подписана цифровой подписью. |
| [get_IsValid](./get_isvalid/)() | Указывает, что строка подписи подписана цифровой подписью и эта цифровая подпись действительна. |
| [get_ProviderId](./get_providerid/)() | Получает или задает идентификатор поставщика подписи для этой строки подписи. Значение по умолчанию — "{00000000-0000-0000-0000-000000000000}". |
| [get_ShowDate](./get_showdate/)() | Получает или задает значение, указывающее, что дата подписи отображается в строке подписи. Значение по умолчанию для этого свойства — **true**. |
| [get_Signer](./get_signer/)() | Получает или задает предложенного подписанта строки подписи. Значение по умолчанию для этого свойства — **empty string**. |
| [get_SignerTitle](./get_signertitle/)() | Получает или задает предложенную должность подписанта (например, Менеджер). Значение по умолчанию для этого свойства — **empty string**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowComments](./set_allowcomments/)(bool) | Сеттер для [Aspose::Words::Drawing::SignatureLine::get_AllowComments](./get_allowcomments/). |
| [set_DefaultInstructions](./set_defaultinstructions/)(bool) | Сеттер для [Aspose::Words::Drawing::SignatureLine::get_DefaultInstructions](./get_defaultinstructions/). |
| [set_Email](./set_email/)(const System::String\&) | Сеттер для [Aspose::Words::Drawing::SignatureLine::get_Email](./get_email/). |
| [set_Id](./set_id/)(System::Guid) | Сеттер для [Aspose::Words::Drawing::SignatureLine::get_Id](./get_id/). |
| [set_Instructions](./set_instructions/)(const System::String\&) | Сеттер для [Aspose::Words::Drawing::SignatureLine::get_Instructions](./get_instructions/). |
| [set_ProviderId](./set_providerid/)(System::Guid) | Сеттер для [Aspose::Words::Drawing::SignatureLine::get_ProviderId](./get_providerid/). |
| [set_ShowDate](./set_showdate/)(bool) | Сеттер для [Aspose::Words::Drawing::SignatureLine::get_ShowDate](./get_showdate/). |
| [set_Signer](./set_signer/)(const System::String\&) | Сеттер для [Aspose::Words::Drawing::SignatureLine::get_Signer](./get_signer/). |
| [set_SignerTitle](./set_signertitle/)(const System::String\&) | Сеттер для [Aspose::Words::Drawing::SignatureLine::get_SignerTitle](./get_signertitle/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
