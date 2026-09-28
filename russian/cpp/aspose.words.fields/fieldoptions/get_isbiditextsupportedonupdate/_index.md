---
title: "Метод Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate"
linktitle: "get_IsBidiTextSupportedOnUpdate"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate. Получает или задает значение, указывающее, поддерживается ли полностью двунаправленный текст во время обновления поля, в C++."
type: docs
weight: 15000
url: /ru/cpp/aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/
---
## FieldOptions::get_IsBidiTextSupportedOnUpdate method


Получает или задает значение, указывающее, поддерживается ли полностью двунаправленный текст во время обновления поля.

```cpp
bool Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate() const
```

## Примечания


Когда это свойство установлено в **true**, выполняются дополнительные шаги для получения результата поля, совместимого с языками справа налево (например, арабский или иврит) во время его обновления.

Когда это свойство установлено в **false** и используется язык справа налево, корректность результата поля после его обновления не гарантируется.

Значение по умолчанию — **false**.

## Примеры



Показывает, как использовать [FieldOptions](../), чтобы обеспечить полную поддержку двунаправленного текста при обновлении полей.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Убедитесь, что любая операция с полем, включающая текст справа налево, выполняется как ожидается.
doc->get_FieldOptions()->set_IsBidiTextSupportedOnUpdate(true);

// Используйте построитель документов, чтобы вставить поле, содержащее текст справа налево.
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"עֶשְׂרִים", u"שְׁלוֹשִׁים", u"אַרְבָּעִים", u"חֲמִשִּׁים", u"שִׁשִּׁים"}), 0);
comboBox->set_CalculateOnExit(true);

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.Bidi.docx");
```

## См. также

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
