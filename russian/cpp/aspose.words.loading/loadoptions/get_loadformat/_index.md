---
title: "Aspose::Words::Loading::LoadOptions::get_LoadFormat метод"
linktitle: "get_LoadFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Loading::LoadOptions::get_LoadFormat метод. Указывает формат загружаемого документа. По умолчанию — Auto в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words.loading/loadoptions/get_loadformat/
---
## LoadOptions::get_LoadFormat method


Указывает формат загружаемого документа. По умолчанию — [Auto](../../../aspose.words/loadformat/).

```cpp
Aspose::Words::LoadFormat Aspose::Words::Loading::LoadOptions::get_LoadFormat() const
```

## Примечания


Рекомендуется указывать значение [Auto](../../../aspose.words/loadformat/) и позволять Aspose.Words автоматически определять формат файла. Если вы знаете формат документа, который собираетесь загрузить, вы можете указать формат явно, и это немного сократит время загрузки, уменьшив накладные расходы, связанные с автоматическим определением формата. Если вы укажете явный формат загрузки, и он окажется неверным, будет выполнено автоматическое определение и будет предпринята вторая попытка загрузить файл.

## Примеры



Показывает, как указать базовый URI при открытии HTML‑документа.
```cpp
// Предположим, что мы хотим загрузить .html‑документ, содержащий изображение, связанное относительным URI
// в то время как изображение находится в другом месте. В этом случае нам потребуется преобразовать относительный URI в абсолютный.
// Мы можем задать базовый URI, используя объект HtmlLoadOptions.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(Aspose::Words::LoadFormat::Html, u"", get_ImageDir());

ASSERT_EQ(Aspose::Words::LoadFormat::Html, loadOptions->get_LoadFormat());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing image.html", loadOptions);

// Хотя изображение было повреждено во входном .html, наш пользовательский базовый URI помог нам восстановить ссылку.
auto imageShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(imageShape->get_IsImage());

// Этот выходной документ отобразит отсутствующее изображение.
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BaseUri.docx");
```

## См. также

* Enum [LoadFormat](../../../aspose.words/loadformat/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
