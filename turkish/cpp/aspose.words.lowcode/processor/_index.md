---
title: "Aspose::Words::LowCode::Processor sınıfı"
linktitle: "Processor"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::LowCode::Processor sınıfı. C++'ta farklı belge işleme eylemlerini gerçekleştirmek için işlemci sınıfı."
type: docs
weight: 1126
url: /tr/cpp/aspose.words.lowcode/processor/
---
## Processor class


[Processor](./) class for performing different document processing actions.

```cpp
class Processor : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Execute](./execute/)() | İşlemci eylemini yürütün. |
| [Execute](./execute/)(System::Threading::CancellationToken) | Belirtilen iptal belirteci kullanılarak belge işleme görevini iptal etmeye izin veren işlemci eylemini yürütün. |
| [From](./from/)(const System::String\&) | İşleme için giriş belgesini belirtir. |
| [From](./from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | İşleme için giriş belgesini belirtir. |
| [From](./from/)(const System::SharedPtr\<System::IO::Stream\>\&) | İşleme için giriş belgesini belirtir. |
| [From](./from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | İşleme için giriş belgesini belirtir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [To](./to/)(const System::String\&) | İşlemci için çıkış dosyasını belirtir. |
| [To](./to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | İşlemci için çıkış dosyasını belirtir. |
| [To](./to/)(const System::String\&, Aspose::Words::SaveFormat) | İşlemci için çıkış dosyasını belirtir. |
| [To](./to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | İşlemci için çıkış akışını belirtir. |
| [To](./to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | İşlemci için çıkış akışını belirtir. |
| [To](./to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](./to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
